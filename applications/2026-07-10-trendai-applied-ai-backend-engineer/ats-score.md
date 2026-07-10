# ATS Score — TrendAI (Trend Micro) / Applied AI Backend Engineer

> Scored by Claude acting as enterprise ATS scanner (Workday/Greenhouse/Lever class).

## Overall Score: 84/100

---

## Dimension Breakdown

| Dimension | Score | Notes |
|---|---|---|
| Required-skill coverage | 7/8 | Python, JavaScript, backend services, cloud-native (AWS), APIs/data pipelines, PostgreSQL/MySQL/RDS, Vector retrieval all present verbatim. Missing: explicit "AI coding assistants." |
| Preferred-skill coverage | 2/8 | Monitoring/observability and PostgreSQL present. Missing: Docker, CI/CD (GitHub Actions), IaC, Azure, Go/Java, Graph DBs. |
| Action verb alignment | ~80% | Resume uses Architected, Built, Engineered, Extended, Boosted, Maintained, Sped up, Hardened — strong overlap with JD's design/implement/build/optimize/integrate/troubleshoot. |
| Domain vocabulary match | 6/8 | Present: backend services, cloud-native, APIs, data pipelines, RAG/vector, scalability, monitoring, high availability. Missing: "AI-SDLC," "observability" (exact term). |
| Hard requirement satisfaction | 4/5 | Degree ✓ (B.Tech IT + MPS AI/ML), backend language ✓ (Python/JS), 0-3 yrs ✓, on-call proxy ✓. Location (Ottawa on-site) is the open risk, not a resume-fixable item. |
| Format compliance | Pass | Single column, standard headings, no tables/images, Jake's section order + approved Summary. One-page fit to be confirmed at compile. |

---

## Detailed Justification — Why This Resume Will Work

### Specific bullet -> JD requirement mapping

- **Resume bullet:** "Boosted query performance 60% ... leading the full MySQL to AWS RDS migration ... production-grade scalability."
  **Maps to JD:** "Data Management: relational and analytical data stores, including PostgreSQL, MySQL, RDS" + "solutions designed for scale using cloud services."
  **Why it works:** Hits three named data stores (MySQL, RDS) and the scale mandate with a hard 60% metric.

- **Resume bullet:** "Built secure RAG pipelines over 100+ confidential documents with vector retrieval ..."
  **Maps to JD:** "Vector/Graph DBs to support complex AI-driven business logic" + "secure backend services."
  **Why it works:** Direct vector-DB + security + AI-business-logic match — the core of an *Applied AI* backend role.

- **Resume bullet:** "Engineered a text-to-SQL chat assistant on FastAPI and DuckDB ... grounded in the live schema ... and enforced SQL safety through parser validation, write-statement blocks, and error-fed retries."
  **Maps to JD:** "APIs and data pipelines" + "AI-driven business logic" + "reviews of AI-generated code with a focus on architectural fit and edge cases."
  **Why it works:** Python backend (FastAPI) + safety-layer edge-case handling maps to both the AI and the quality responsibilities.

- **Resume bullet:** "Maintained 99.9% system uptime ... AWS EC2 and S3 with real-time monitoring dashboards ... resolving production incidents."
  **Maps to JD:** "integrated monitoring and observability," "high availability," "on-call rotations."
  **Why it works:** Covers three preferred/ops requirements at once.

### Keyword landing report

- "**AWS**" appears in: Summary, Experience (Dots N Key), Projects (ETL), Skills — quadruple-weighted.
- "**Python**" appears in: Projects (FastAPI/ETL) and Skills > Languages.
- "**MySQL / RDS / PostgreSQL**" appear in: Experience bullet 1 (with metric) and Skills > Cloud & Databases.
- "**RAG / vector**" appears in: Summary, Experience, Projects, Skills > AI/ML.
- "**FastAPI / Node.js / APIs**" appear in: Experience, Projects, Skills > Frameworks.

### Format/parsing predictions

- Single column -> parses cleanly across Workday/iCIMS/Taleo (no multi-column risk).
- No tables, headers/footers, or images -> no parser failure modes.
- Standard section headings ("Experience," "Education," "Projects," "Technical Skills") -> section detection succeeds. (The added "Summary" heading is standard and ATS-safe.)

---

## What Could Still Improve

1. **Add an explicit "AI coding assistants" signal** (Claude Code / Cursor / Copilot) if true — it is the JD's most-emphasized requirement and the one clear required-skill miss. Biggest single score lever (would push toward ~90).
2. **Surface the testing signal** — the "~210 Vitest + pytest suites" bullet (seaweed Software Developer variant) directly answers "produce and maintain automated tests ... Python-based frameworks." Consider swapping it into the AI project block.
3. **Docker / GitHub Actions / IaC** — adding any that are true would lift preferred-skill coverage from 2/8.

---

## Score Threshold Interpretation

- **85+:** Ready for external scanner verification + submission
- **70-84:** Iterate on Stage 3 (tailoring) with specific recommendations above  <- **you are here (84), one AI-tooling line from 85+**
- **<70:** Re-run Stage 2 (gap analysis)
