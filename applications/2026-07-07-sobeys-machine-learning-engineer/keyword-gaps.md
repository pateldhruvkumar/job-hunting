# Keyword Gaps — Sobeys, Machine Learning Engineer

> Keywords from the JD that are NOT backed by your master database files.
> The skill did NOT silently insert these into the tailored resume.

## Real Gaps

### LangGraph / LangChain
**JD context:** "Proven multiple implementation experience with LangGraph and developing LLM-driven compound agentic system." (a hard requirement, and the #2 keyword)
**Status:** Not present in the database. You have built real agents (Vault AI Due Diligence Agent, Multi-Company Comparison Agent, Kahoot Bot), but they are described with n8n orchestration and custom LLM pipelines — LangGraph/LangChain are never named.

**Three options:**
1. **Address in cover letter** — position your hands-on agentic work (autonomous multi-source agent, n8n orchestration, text-to-SQL with retrieval) as directly transferable and note you are ramping on LangGraph specifically.
2. **Add to Skills only if true** — if you have in fact used LangGraph/LangChain in any of these agents, add it and I will re-tailor. Do NOT add it otherwise; it is the single most-checked requirement here.
3. **Acknowledge the gap honestly** — this is the biggest risk in the application. Everything else about agentic systems is strong; the specific framework name is the gap.

### MLflow / Databricks / Snowflake (MLOps tooling)
**JD context:** "Proficiency in MLOps tools and frameworks (e.g., MLflow, Databricks, Snowflake)."
**Status:** Not in the database. You have production/deployment experience (AWS EC2/S3, 99.9% uptime, monitoring dashboards, serverless ETL) but none of these named MLOps platforms.

**Three options:**
1. **Address in cover letter** — frame AWS production deployment + monitoring + CI/CD as MLOps foundations you would extend to MLflow/Databricks.
2. **Add to Skills only if true** — add any you have actually used.
3. **Acknowledge the gap** — "e.g." softens it; the concept (production ML/monitoring) matters more than the exact vendor.

### FAISS / Databricks Vector Search (named vector databases)
**JD context:** "Solid understanding of vector databases (e.g., FAISS, Databricks Vector Search)."
**Status:** You have real vector retrieval and sentence embeddings (RAG over 100+ docs; bge-small-en-v1.5 indexing ~41,000 values), but no FAISS or Databricks Vector Search by name.
**Note:** This is mostly covered by the "Loose Matches" section below — the concept is backed, only the specific product names are missing.

### Azure
**JD context:** "Familiarity with cloud platforms (Azure preferred, GCP, AWS) is strongly recommended."
**Status:** You have strong AWS experience (EC2, S3, Lambda, Glue, RDS, DynamoDB) but no Azure. The JD accepts AWS ("GCP, AWS ... strongly recommended"), so AWS satisfies the recommendation even though Azure is "preferred."

**Three options:**
1. **Rely on AWS** — it satisfies the "strongly recommended" cloud bar; leave as-is.
2. **Address in cover letter** — note cloud skills transfer across providers.
3. **Add Azure to Skills only if true.**

### 4+ years of industry Object-Oriented Python (hard requirement)
**JD context:** "4+ years of industry level expertise in Object-Oriented Python development with production-grade software design patterns."
**Status:** Partial. Your Python is strong and recent (Vault AI agents, FastAPI text-to-SQL service, serverless ETL, PyTorch/NLP projects), but much of your earliest industry tenure (Dots N Key, Unistar) was PHP / Node.js / React, not Python. Total *industry Python* experience is likely under 4 years.

**Three options:**
1. **Emphasize depth over years** — your Python spans agentic systems, RAG, fine-tuning, FastAPI services, and data pipelines; let breadth + recency carry it.
2. **Address in cover letter** — combine total software-engineering tenure (production systems since 2022) with focused Python/ML depth.
3. **Acknowledge the gap** — a recruiter may screen on the literal "4+ years Python." Worth a candid framing.

---

## Loose Matches (cautious use — verify before submitting)

### Agentic systems (vs. LangGraph specifically)
**JD context:** "develop conversational / process automation agents"; "build and maintain Lang chain-based agentic applications."
**Closest match in master:** "Engineered an autonomous Due Diligence Agent that orchestrates multi-source web research..."; "Designed a Multi-Company Financial Comparison Agent..."; "Shipped an agentic AI quiz automation ... with n8n orchestrating 3 open-source APIs."
**Skill's note:** The *capability* (building autonomous, tool-using agents) is strongly backed; only the LangGraph/LangChain framework is not named. Kept the agent bullets; did NOT claim LangGraph.
**Your decision:** Accept (agents are real) — confirmed in resume.

### Vector databases (vs. FAISS / Databricks Vector Search)
**JD context:** "Solid understanding of vector databases (e.g., FAISS, Databricks Vector Search) and LLM retrieval techniques (e.g., RAG)."
**Closest match in master:** "Built secure RAG pipelines over 100+ confidential documents with vector retrieval"; "Indexed roughly 41,000 distinct entity values with BAAI/bge-small-en-v1.5 sentence embeddings."
**Skill's note:** RAG and vector retrieval/embeddings are directly backed; used "Vector retrieval" and "RAG" in the resume rather than a specific product name.
**Your decision:** Accept — confirmed in resume.

### Mentoring / leading AI/ML projects
**JD context:** "Having experience leading AI/ML projects or mentoring junior engineers would be looked at with priority."
**Closest match in master:** "Led backend performance, cloud infrastructure, and full-stack optimization..."; "leading a full MySQL to AWS RDS migration."
**Skill's note:** Leadership of technical projects is backed; explicit *mentoring of junior engineers* is not in the database. Kept "Led" bullets; did NOT claim mentoring.
**Your decision:** Accept the leadership framing; mentoring stays out unless true.

---

## Master Database Updates Suggested

If any "Real Gap" above is actually an experience you have (especially **LangGraph/LangChain**, **MLflow/Databricks/Snowflake**, or **Azure**), add it to the relevant `database/master-*.md` file and I will re-run Stage 3. LangGraph in particular would materially strengthen this application.
