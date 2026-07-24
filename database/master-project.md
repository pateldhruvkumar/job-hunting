# Master Projects

> Canonical project record. Use this file as the source of truth when tailoring resumes for specific job applications. Companion to `master-experience.md`.
>
> **Special rule for the flagship project below:** the Seaweed Market Intelligence Dashboard has three role-specific variants (Data Analyst, Software Developer, AI Engineer). Any given resume must use **exactly one** variant — pick the one matching the target role.

---

## Flagship: Seaweed Market Intelligence Dashboard (three role-specific variants) Apr 2026 - Jun 2026

One project, three interchangeable presentations. Each variant below is self-contained with its own resume title, tech-stack line, and bullet set.

### Data Analyst variant — Global Seaweed Market Analytics Dashboard | Python, DuckDB, React

- Consolidated 11 raw datasets (33,000+ records) from FAO FishStat, Statistics Canada, and UN Comtrade into a single DuckDB analytical layer covering seaweed production across 100+ countries from 1950 to 2024.
- Scripted a Python preprocessing pipeline that reshaped 4 FAO tables (27,000+ rows) into 35 chart-ready JSON files, letting all 13 dashboard tabs load from static data with zero runtime queries.
- Designed 13 analytical views spanning 7 visualization types, including a country-by-species heatmap that exposes how heavily global supply concentrates in China, Indonesia, and the Philippines.
- Tracked Canadian industry KPIs (export value, price per wet tonne, value per pound, gross output) against StatCan trade and value-added accounts spanning 2010-2023.
- Flagged a data gap most analyses miss: Canada publishes no seaweed-specific production statistics, so every proxy metric derived from all-aquaculture data carries an in-dashboard source note and caveat.
- Automated stakeholder reporting with one-click Excel workbooks per tab, one sheet per dataset plus an About sheet carrying citations and caveats, generated client-side with SheetJS.

### Software Developer variant — Seaweed Industry Intelligence Platform | React 18, FastAPI, Vite

- Developed a 52-component React 18 dashboard (roughly 8,900 lines of JSX) with Vite, Tailwind, Recharts, and Plotly, organized into 13 tabs behind shared year-range, country, and species filters.
- Shipped one-click export to PDF, PowerPoint, and Excel entirely in the browser using jsPDF, pptxgenjs, and SheetJS, producing branded documents with logos, source citations, and page numbers without a server round trip.
- Deferred loading of all three export libraries until the user actually clicks download, keeping them out of the initial bundle.
- Wrote roughly 210 tests across 25 Vitest and React Testing Library files covering chat UI, export generation, and custom hooks, plus 5 pytest suites for the FastAPI backend.
- Stood up an async FastAPI service that loads 4 CSV tables into in-memory DuckDB at startup and serves a chat endpoint with health checks and structured error responses.
- Adapted the layout for mobile by collapsing the docked sidebar and chat panel into full-screen overlays below the large breakpoint.

### AI Engineer variant — AI-Powered Seaweed Market Intelligence Dashboard | LLM Text-to-SQL, Embeddings, FastAPI

- Engineered a text-to-SQL chat assistant on FastAPI and DuckDB in which Qwen3.6-35B (via OpenRouter) generates queries against a 27,000-row FAO dataset, grounded in the live schema, retrieved entities, and few-shot examples.
- Indexed roughly 41,000 distinct entity values (country, species, and region names) with BAAI/bge-small-en-v1.5 sentence embeddings, resolving fuzzy user phrasing to exact database values at a 0.75 similarity threshold.
- Curated 22 question-to-SQL exemplars and retrieved the 3 most similar per query, steering generation toward dataset-specific patterns like NULLIF guards on division and NULLS LAST rankings.
- Enforced SQL safety in three layers: parser validation restricting output to a single SELECT, hard blocks on write statements, and up to 3 retries that feed the DuckDB error message back to the model.
- Built an enrichment pass in which a second LLM call summarizes results, proposes 2-3 follow-up questions, and picks a chart type the frontend renders automatically, degrading to a plain table if the call fails.
- Trimmed token spend by disabling model reasoning for the SQL step and capping conversation history at the last 10 messages.

### Full project narrative (reference — not resume copy)

Canonical story of the project in Dhruv's own words. Use this for cover letters, interview prep, and behavioral answers; the resume bullets above are derived from it.

**1. Data sourcing (~2 weeks).** Spent two weeks finding a dataset that could actually make a difference in the seaweed market. Landed on two sources:

- **FAO:** global production, capture quantity, aquaculture quantity, and aquaculture value.
- **Statistics Canada:** canada_interprovincial_trade, canada_aquaculture_production_value, canada_aquaculture_valueadded, canada_ns_leases, canada_ns_rockweed, canada_seaweed_exports, and canada_bc_aqua_sites.

Total: ~33,700 data rows across 11 CSVs.

**2. Data pipeline and EDA.** Followed the standard pipeline: data summary, cleaning, analysis, then a full EDA once the shape of the data was understood.

**3. KPIs (21 total).** Built KPIs across five groups: Canada Economics, Canada Licensing, Gross Output, Export Value, and Value Per lb.

- Preprocessing: Python (pandas + NumPy) turning the CSVs into JSON, tested with pytest.
- Frontend: React 18 (useData + useMemo), plain JavaScript for the KPI math, a reusable KpiCard component, Tailwind CSS with lucide-react icons, Recharts for charts, built with Vite and tested with Vitest.

**4. AI chatbot (user-facing).** Takes a plain-English prompt and returns an answer with context, a graph, a table, and the SQL query used, so the user can verify the result.

**5. AI chatbot (behind the scenes).** At startup (once):

- Load the FAO seaweed CSVs into an in-memory DuckDB database.
- Load a small embedding model (bge-small-en-v1.5) that turns text into vectors.
- Pre-embed two things: every real data value (country/species names) and a set of example question→SQL pairs.

Per question:

- Entity matching: match the question against the pre-embedded data values to find the exact spellings that exist in the data (so "korea kelp" maps to the real names in the tables).
- Few-shot retrieval: pull the 3 most similar past question→SQL examples to guide the model.
- Prompt build: combine the database schema, the matched entities, the examples, and the last 10 messages of chat history.
- SQL generation: the LLM (Llama 3.3 70B via Groq) writes a SQL query from that context.
- Safety check: reject anything that isn't a read-only SELECT before it runs.
- Execution: run the query against DuckDB to get real numbers.
- Answer: a single number is formatted directly; a table of rows gets a second LLM call to summarize it in one sentence.
- Return everything: the plain-English answer, the generated SQL, and the raw data (so the frontend can also draw a chart/table).

**6. Export feature.** Added an Export button to every dashboard tab:

- Download a tab as PDF, PowerPoint, or Excel — entirely in the browser, no backend needed.
- Captures chart images and embeds them in the PDF and PowerPoint files.
- PDF = branded report with logo, header, and footer. PowerPoint = branded slide deck (title slide + one slide per chart). Excel = the actual raw data plus a sources sheet.
- Source citations are preserved in every exported file.
- Export libraries load only on click, so the app stays fast; export is blocked while a tab is loading and double-clicks are debounced.
- Libraries: jsPDF (PDF), pptxgenjs (PowerPoint), SheetJS (Excel), html-to-image + Plotly (chart images).

**7. Deployment.**

- **Frontend:** Vercel, static React/Vite build, live at seaweed-industry.vercel.app. All dashboard tabs, charts, KPIs, and Excel export run entirely client-side from pre-computed JSON — the visualization layer needs no server.
- **Backend:** FastAPI service (DuckDB + embedding model + Groq LLM) powering the AI chatbot. Runs locally via Uvicorn on port 8000; deployable to any Python host (Railway/Fly.io/Render) by setting GROQ_API_KEY and pointing the frontend at the hosted URL.
- **Architecture:** Decoupled frontend/backend — the static dashboard is independent of the AI service, so the core product stays fast and always available even if the chatbot backend is offline.

---

## Other Projects

### Olist E-Commerce Logistics & Margin Optimization Pipeline | Python, PostgreSQL (Supabase), SQL, Excel, Power BI (DAX) | Jul 2026

- Built an end-to-end analytics pipeline that moved 100K+ Olist Brazilian e-commerce records from 9 raw Kaggle CSVs into a live cloud Supabase PostgreSQL database using a Python and SQLAlchemy loader with chunked, multi-row bulk inserts, replacing flat-file analysis with a queryable relational source.
- Engineered a SQL master view joining orders, order_items, customers, and products that derives delivery_delay_days from the gap between actual and estimated delivery dates, handles nulls, and filters to delivered orders, so every downstream tool consumed clean, pre-calculated data instead of raw tables.
- Developed a dynamic Excel unit-economics "What-If" model on PivotTables covering all 27 Brazilian states, driving projected freight and per-order margin loss from a single carrier-rate parameter cell with absolute references, giving the operations team a sandbox to test carrier pricing scenarios.
- Quantified freight-cost sensitivity with the model, showing a 20% carrier rate hike adds $8.01 of freight cost per order in remote Acre versus just $3.02 in São Paulo, translating an abstract rate change into concrete per-state margin impact.
- Modeled the Power BI dataset as a star schema, building a dynamic DAX date dimension with CALENDARAUTO and linking it one-to-many to the logistics fact table to unlock time-intelligence analysis across 2016 to 2018 via a year slicer.
- Centralized business logic in a dedicated DAX measures table, including an SLA Breach Rate measure that divides late orders (delivery_delay_days > 0) by total orders, exposing a 7% nationwide breach rate against 60K total orders and an 11-day average early-delivery buffer.
- Implemented a custom Brazil Shape Map hardcoded to national geometry to bypass Bing Maps misreading Brazilian state codes as US states (e.g., AL as Alabama, not Alagoas), with red/green conditional formatting on SLA breach rate for instant, pre-attentive reading of failure hotspots.
- Surfaced actionable logistics insights: freight-to-price ratios above 50% in remote northern states (Rondônia 59.6%, Roraima 56.8%, Maranhão 55.0%) versus 26.5% in São Paulo, and heavy/bulky categories such as furniture as the main drivers of nationwide delivery delays, pointing to a need for a specialized oversized-freight partner.

### Vancouver International Airport (YVR) — Capstone | Jan 2026 – Apr 2026

- Designed a 7-tab Streamlit dashboard on 183,909 cleaned charging sessions spanning 56 PosiCharge DVS 400 chargers, giving YVR operations real-time visibility into charger health for a 260-vehicle electric ground-support fleet.
- Engineered a Weighted Ensemble forecasting model (Random Forest + XGBoost + LightGBM) on 33 derived time, lag, flight, and weather features, hitting 84.7% binary accuracy and a 28% MAE reduction (15.26 → 10.94) over a 2-month baseline.

### AWS Big Data Pipeline – Serverless ETL Architecture | AWS S3, Lambda, Glue, DynamoDB | Jan 2026 - Mar 2026

- Built an end-to-end serverless ETL pipeline in Python on AWS (S3, Lambda, Glue, DynamoDB) to ingest, validate, deduplicate, and load 5.6M user records, fully automating a previously hands-on workflow.
- Cut batch insert time by 40% by parallelizing ingestion logic with memory-efficient data structures across distributed Lambda functions for high-throughput processing under concurrent-execution constraints.

### eHealth – Full-Stack Analytics Platform | Node.js, React.js, MongoDB, AWS | Jan 2026 - Feb 2026

- Designed a microservice health analytics platform in Node.js, React.js, and MongoDB with ML prediction models on AWS CI/CD, lifting adoption by 50% and cutting prescription errors by 30% through clinical decision support.

### Steve's and Associates — Capstone | Sep 2025 – Dec 2025

- Developed a Python data-transformation pipeline with TF-IDF, K-Means, and LDA topic modeling (scikit-learn) that surfaced 7 key business themes and cut manual categorization effort by 70%, freeing analysts for higher-value work.
- Streamlined data ingestion scripts in Python and SQL to transform 6 fiscal years of billing data over 50+ enterprise clients, defining KPI metrics and accelerating executive report generation by 40%.

### Offensive Language Detection – Deep Learning NLP | Python, PyTorch, ULMFiT, TF-IDF | Oct 2025

- Hit 82% macro-F1 on offensive-speech classification with a ULMFiT transfer-learning pipeline in PyTorch, benchmarked against TF-IDF on the OLID dataset (14K+ labeled samples) to quantify the pretrained-model advantage.
- Trimmed model training time by 30% through an optimized hyperparameter search strategy and a refactored data-preprocessing pipeline, speeding experimentation cycles without sacrificing classification accuracy.

### Kahoot Bot – Agentic AI Automation | Python, n8n, REST APIs | Aug 2025

- Shipped an automated AI quiz system in Python with n8n orchestrating 3 open-source APIs, hitting 90% accuracy while cutting inference costs by 60% via optimized call sequencing; placed 2nd of 15+ teams at Northeastern's Agentic AI 2.0 Hackathon.


## Inventory Analyst Projects

### Charging Demand Forecast, Vancouver International Airport (Capstone)	Jan 2026 - Apr 2026

- Engineered a weighted ensemble forecasting model (Random Forest, XGBoost, LightGBM) on 33 time, lag, flight, and weather features, reaching 84.7% accuracy and cutting forecast error 28%.
- Processed 183,909 charging sessions across 56 chargers into a clean modeling dataset, giving operations demand visibility for a 260-vehicle electric ground-support fleet.
- Delivered a 7-tab Streamlit dashboard surfacing real-time demand and asset-health signals so planners could anticipate shortfalls before they hit operations.


### Global Seaweed Market Analytics Dashboard	Apr 2026 - Jun 2026

- Consolidated 11 datasets (33,000+ records) from FAO, Statistics Canada, and UN Comtrade into a single DuckDB analytical layer covering supply across 100+ countries.
- Tracked industry KPIs including export value, price per tonne, value per pound, and gross output across 2010 to 2023 to expose supply concentration and pricing trends.
- Automated stakeholder reporting with one-click Excel workbooks across 13 dashboard views, each carrying source citations and data-quality caveats, replacing manual spreadsheet prep.
