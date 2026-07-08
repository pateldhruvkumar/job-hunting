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

---

## Other Projects

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
