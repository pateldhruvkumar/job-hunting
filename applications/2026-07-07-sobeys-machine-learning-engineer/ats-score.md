# ATS Score — Sobeys, Machine Learning Engineer

> Scored by Claude acting as enterprise ATS scanner (Workday/Greenhouse/Lever class).

## Overall Score: 70/100

Strong, genuine match on the AI substance (agentic systems, LLMs, RAG, vector retrieval, production cloud) but held back by three items tailoring alone cannot fix: the missing **LangGraph** hard requirement, no named **MLOps platforms** (MLflow/Databricks/Snowflake), and a **location mismatch** (candidate in Vancouver; role is Toronto-hybrid).

---

## Dimension Breakdown

| Dimension | Score | Notes |
|---|---|---|
| Required-skill coverage | 4.5/8 | Solid: LLMs, RAG, Agentic AI. Partial (concept but not verbatim/named): Object-Oriented Python, Vector databases, MLOps, ML system design. Missing: LangGraph/LangChain. |
| Preferred-skill coverage | 2.5/5 | Present: deploying fine-tuned LLMs (QLoRA Llama), cloud (AWS). Partial: leading AI/ML projects. Missing: mentoring junior engineers, operations research algorithms. |
| Action verb alignment | 72% | Resume verbs (Engineered, Designed, Built, Fine-tuned, Shipped, Led, Deployed) overlap well with JD's build/design/develop/deploy/automate. |
| Domain vocabulary match | 5/8 | Hits: retail (POS/high-traffic retail operations), RAG, embeddings, vector retrieval, agentic. Misses: "compound agentic system", "enterprise data architecture", "operations research". |
| Hard requirement satisfaction | 1.5/4 | Degree in CS/related ✓ (B.Tech IT + MPS Data Analytics). LangGraph implementations ✗. 4+ yrs industry OOP Python — partial/under. Toronto-hybrid location ✗ (candidate in Vancouver, BC). |
| Format compliance | Pass | Single column, standard headings, no tables/images/columns, XYZ bullets. One-full-page fit pending LaTeX compile. |

---

## Detailed Justification — Why This Resume Will Work

### Specific bullet -> JD requirement mapping

- **Resume bullet:** "Engineered an autonomous Due Diligence Agent that orchestrates multi-source web research, synthesizing credit-risk and legal-compliance findings into production-ready PDF reports..."
  **Maps to JD:** "develop conversational / process automation agents"; "develop and maintain end-to-end Agentic AI/ML solutions."
  **Why it works:** A real, shipped autonomous agent with tool use and a production output. Strongest evidence of agentic capability short of naming LangGraph.

- **Resume bullet:** "Built secure RAG pipelines over 100+ confidential documents with vector retrieval and sentence embeddings, grounding LLM answers..."
  **Maps to JD:** "Solid understanding of vector databases ... and LLM retrieval techniques (e.g., RAG)."
  **Why it works:** RAG appears verbatim with quantified scale (100+ docs) and the exact mechanism (vector retrieval + embeddings) the JD asks about.

- **Resume bullet:** "Fine-tuned Llama models with QLoRA on domain-specific terminology, improving answer accuracy 15% on internal evaluations."
  **Maps to JD:** "Experience deploying LLMs or fine-tuned models in production environments is a significant asset."
  **Why it works:** Directly satisfies a named "significant asset" with a quantified result.

- **Resume bullet:** "Boosted query performance 60% ... by leading a full MySQL to AWS RDS migration ... for high-traffic retail operations."
  **Maps to JD:** Sobeys domain (grocery retail) + "scalable, maintainable" production systems + cloud recommendation.
  **Why it works:** Retail-domain production engineering on cloud — rare, directly relevant context for a grocery retailer's ML platform team.

### Keyword landing report

- "**RAG**" appears in: Experience bullet (Vault AI) AND Technical Skills (AI/ML row) — double-weighted.
- "**Agentic AI**" appears in: Summary, two Experience bullets, a Project title, AND Technical Skills — heavily weighted.
- "**LLMs / LLM fine-tuning**" appears in: Summary, Experience, Projects, AND Skills.
- "**Vector retrieval / embeddings**" appears in: Experience, Projects, AND Skills.
- "**AWS / cloud**" appears in: Experience (EC2/S3/RDS), Projects (Lambda/Glue/DynamoDB), AND Skills.
- "**Python**" appears in: Projects AND Skills (Languages, first position).
- **Missing keywords (will not land):** LangGraph, LangChain, MLflow, Databricks, Snowflake, FAISS, Azure, "operations research", "compound agentic system", "ML system design" (verbatim).

### Format/parsing predictions

- Single column -> parses cleanly across Workday/iCIMS/Taleo (no multi-column risk).
- No tables, no headers/footers, no images -> no parser failure modes.
- Standard section headings ("Education", "Experience", "Projects", "Technical Skills") -> section detection succeeds.
- Summary section added at top -> parses as a text block; no ATS risk.

---

## What Could Still Improve

1. **LangGraph is the highest-leverage fix.** It is a stated hard requirement and the JD's #2 keyword. If you have used LangGraph/LangChain in any agent, add it to the database and I will re-tailor — this single change would likely move the score into the 80s.
2. **MLOps vendor names.** If you have touched MLflow, Databricks, or Snowflake (even in coursework/projects), add them. The concept is adjacent to your AWS + monitoring + serverless-ETL work but the named tools do not currently land.
3. **Location.** The role is Toronto-hybrid; your profile lists Vancouver, BC. Not an ATS keyword issue, but a recruiter screen will catch it. Decide whether to signal relocation/hybrid flexibility in the cover letter.
4. **"Object-Oriented Python" verbatim.** The phrase itself does not appear. If accurate, a FastAPI/service-design bullet could be reworded to name modular/OOP design explicitly — only if it stays true to the work.

---

## Score Threshold Interpretation

- **85+:** Ready for external scanner verification + submission
- **70-84:** Iterate on Stage 3 (tailoring) with specific recommendations above  <- **this resume is here (70)**
- **<70:** Re-run Stage 2 (gap analysis) — gap may be deeper than tailoring can fix

**Verdict:** Submit-worthy on substance, but the LangGraph/MLOps gaps and Toronto location are real. The biggest score gains come from database updates (if the experience exists), not further wordsmithing.
