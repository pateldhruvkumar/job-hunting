# Keyword Gaps — HelloFresh Machine Learning Engineer, Operations Technology

> Keywords from the JD that are NOT backed by your master database files.
> The skill did NOT silently insert these into the tailored resume.

## Real Gaps

### MLFlow
**JD context:** "Experience with modern MLOps tooling such as MLFlow, feature engineering, Kubernetes, and workflow orchestration" and "MLOps platform ... built on Databricks, MLFlow, and Prefect."
**Status:** Not present in the database files.

**Three options:**
1. **Address in cover letter** as ramping on MLFlow — you have hands-on ML lifecycle work (fine-tuning, evaluations, ensemble modeling) that maps directly onto MLFlow's tracking/registry concepts.
2. **Add to Skills** as `Familiar with: MLFlow` — only if you have actually touched it.
3. **Acknowledge gap honestly** — this is a "such as" preferred item, not a knockout; your underlying ML lifecycle experience is the substance the tool wraps.

### Databricks
**JD context:** "MLOps platform ... built on Databricks" and "Experience with PySpark and Databricks is a plus."
**Status:** Not present. Explicitly flagged "a plus," so not a knockout.

**Three options:**
1. **Address in cover letter** briefly as a platform you are eager to pick up, anchored to your AWS + data-pipeline experience.
2. **Add to Skills** as `Familiar with: Databricks` — only if true.
3. **Acknowledge gap honestly** — "a plus," low risk.

### PySpark
**JD context:** "Experience with PySpark and Databricks is a plus."
**Status:** Not present. You have Python + large-dataset pipeline work (5.6M records on AWS, 33K+ record DuckDB layer) but not Spark specifically.

**Three options:**
1. **Address in cover letter** — connect to your distributed AWS Lambda ingestion and large-dataset ETL.
2. **Add to Skills** as `Familiar with: PySpark` — only if true.
3. **Acknowledge gap honestly** — "a plus," low risk.

### Kubernetes
**JD context:** "modern MLOps tooling such as MLFlow, feature engineering, Kubernetes, and workflow orchestration."
**Status:** Not present. You have AWS EC2/S3 deployment and serverless (Edge Functions, Lambda) but no container-orchestration evidence.

**Three options:**
1. **Address in cover letter** as an area you are actively learning, anchored to your production AWS deployment experience.
2. **Add to Skills** as `Familiar with: Kubernetes` — only if true.
3. **Acknowledge gap honestly** — one item in a "such as" list.

### Image Generation
**JD context:** "agentic GenAI system that integrates with HelloFresh's culinary content pipeline (API development, LLM orchestration, image generation)" and "Familiarity or interest in generative AI (LLMs, image generation ...)."
**Status:** Not present. Your GenAI work is text/LLM/RAG and TTS/audio, not image generation.

**Three options:**
1. **Address in cover letter** as an interest — the JD asks for "familiarity or interest," so stated interest plus your strong text-GenAI base is a reasonable answer.
2. **Add to Skills** — only if you have actually built an image-generation feature.
3. **Acknowledge gap honestly** — framed as "interest," this is satisfiable without fabrication.

### Drift Detection
**JD context:** "Improve operational excellence through automation, monitoring, drift detection, and data quality practices."
**Status:** Not present as a named practice. You have monitoring (Dots N Key uptime dashboards), data quality (Operations Data Assistant), and model evaluation (QLoRA internal evals) but not "drift detection" specifically.

**Three options:**
1. **Address in cover letter** under operational excellence, tying to your monitoring + data-quality + model-evaluation experience.
2. **Add to Skills** — only if true.
3. **Acknowledge gap honestly** — adjacent experience is strong; the exact term is the gap.

---

## Loose Matches (cautious use — verify before submitting)

### Workflow orchestration (Prefect)
**JD context:** "workflow orchestration (e.g., Prefect)" and "MLOps platform ... built on ... Prefect."
**Closest match in database:** Kahoot Bot — "n8n orchestrating 3 open-source APIs"; Vault AI agents "orchestrate multi-source web research."
**Skill's note:** n8n is a workflow-orchestration tool in the same family as Prefect; "orchestration" is genuinely backed, but Prefect itself is not. The resume surfaces "agentic workflows" and "orchestration," not "Prefect."
**Your decision:** Accept / reject the orchestration framing (kept in resume as "agentic workflows / orchestration"; Prefect NOT claimed).

### Test-driven development (TDD)
**JD context:** "test-driven development (TDD), spec-driven development."
**Closest match in database:** Seaweed platform — "roughly 210 tests across 25 Vitest and React Testing Library files ... plus 5 pytest suites."
**Skill's note:** Strong automated-testing evidence, but the database does not state the tests were written test-first (TDD) or spec-driven. The resume does NOT claim "TDD" verbatim; testing rigor is demonstrated through the Seaweed project (not currently on this one-page cut) and can be raised in the cover letter or interview.
**Your decision:** Accept / reject — confirm before claiming "TDD" as a verbatim skill.

### CI/CD
**JD context:** "model serving, monitoring, and CI/CD pipelines."
**Closest match in database:** eHealth project — "microservice health analytics platform ... on AWS CI/CD"; Vault AI Git feature-branch and pull-request workflow.
**Skill's note:** CI/CD is backed by the eHealth project; listed in Skills. Reasonable to keep.
**Your decision:** Accept (kept in Skills as "CI/CD").

---

## Fit note (not a keyword, but flag before submitting)

- **Location:** You are in Vancouver, BC; this role is Toronto, ON hybrid (minimum 2 days/week in office). The resume shows your real location. Decide whether to signal willingness to relocate — I did not assert relocation in the cover letter because it is not in the database. Tell me if you want a relocation line added.

---

## Master Database Updates Suggested

If any "Real Gap" above (MLFlow, Databricks, PySpark, Kubernetes, image generation, drift detection) is actually something you have done, add it to the relevant `database/*.md` file and re-run the tailoring stage — it would materially strengthen this application.
