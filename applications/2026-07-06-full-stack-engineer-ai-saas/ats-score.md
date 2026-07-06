# ATS Score — Unnamed Enterprise AI SaaS Startup, Full Stack Engineer

> Scored by Claude acting as enterprise ATS scanner (Workday/Greenhouse/Lever class).

## Overall Score: 85/100

---

## Dimension Breakdown

| Dimension | Score | Notes |
|---|---|---|
| Required-skill coverage | 8/9 | AI agents, full stack, backend, APIs, web UI, LLMs, production, internal tools all present. Missing: AI coding tools (Claude Code/Cursor/Codex) - named requirement, real gap. |
| Preferred-skill coverage | 1/3 | Portfolio link partially covers design taste. "Early-stage startup" not claimed (master lacks evidence). Design-craft resources not resume material. |
| Action verb alignment | ~70% | Built, Shipped (2x), Designed, Implemented, Delivered mirror JD verbs. JD's "architect" and "partner" unused. |
| Domain vocabulary match | 5/8 | AI agents, LLMs, internal tools, production, agent workflow (n8n) present. "Enterprise", "SaaS", "agent frameworks" absent as literal strings. |
| Hard requirement satisfaction | 4/4 | ~2.3 yrs professional dev experience (in 2-4 band); Vancouver BC = Canada remote-eligible; production systems (POS platform, uptime bullet); frontend + backend both evidenced. |
| Format compliance | Pass | Single column, no tables/images/icons, standard section headings, contact in body, `\pdfgentounicode=1` set for machine-readable PDF. |

---

## Detailed Justification — Why This Resume Will Work

### Specific bullet → JD requirement mapping

- **Resume bullet:** "Shipped an autonomous due-diligence AI agent that runs multi-source web research and compiles credit-risk and legal-compliance findings into client-ready PDF reports."
  **Maps to JD:** "Design, build, and implement AI agents, backend services, APIs and web UIs"
  **Why it works:** Verbatim "AI agent" hit in the first visible role, with a concrete production artifact (client-ready reports), in an enterprise fintech domain that mirrors "enterprise AI SaaS."

- **Resume bullet:** "Cut query latency 60% on the SONAR retail POS platform by leading a full MySQL to AWS RDS migration, removing a single point of failure from production."
  **Maps to JD:** "You've built and maintained production systems used by real users"
  **Why it works:** Quantified (60%), names a real production system with real users, and shows ownership of an infrastructure decision end-to-end.

- **Resume bullet:** "Developed a 52-component React dashboard (roughly 8,900 lines of JSX)... organized into 13 tabs behind shared year-range, country, and species filters."
  **Maps to JD:** "You're happy moving across frontend and backend when needed" / "web UIs"
  **Why it works:** Concrete frontend scale (52 components, 13 tabs) paired in the same project with an async FastAPI backend and a real test suite - the exact frontend+backend spread the JD asks for.

- **Resume bullet:** "Diagnosed and rewrote a faulty cost-calculation query in the internal operations database, correcting pricing logic and saving thousands of dollars in annual order spend."
  **Maps to JD:** "design and build internal tools to streamline operations and eliminate manual workflows"
  **Why it works:** Internal-operations tooling with a dollar outcome, matching the cross-functional internal-tools half of the role.

### Keyword landing report

- "**AI agents**" appears in: Technical Skills AND two Experience bullets AND a Project title ("Agentic AI") - multi-section hits are double-weighted by most ATS
- "**LLM**" appears in: Experience bullet (fine-tuned Llama LLMs) AND Technical Skills (LLM fine-tuning)
- "**full stack**" appears in: Experience bullet with quantified context ("across the full stack")
- "**production**" appears in: two Experience bullets (migration, uptime)
- "**React / Node.js / FastAPI / AWS**" appear in: Technical Skills AND supporting Experience/Project bullets
- "**RAG / vector embeddings**" appear in: Experience bullet AND Technical Skills

### Format/parsing predictions

- Single column, standard headings (Education, Experience, Projects, Technical Skills) → section detection succeeds across Workday/iCIMS/Taleo
- No tables (LaTeX `tabular*` renders as plain text lines in PDF extraction), no headers/footers, no images → no parser failure modes
- Dates in "Mon YYYY -- Mon YYYY" format → tenure computation parses cleanly

---

## What Could Still Improve

1. **Close the AI-tooling gap (biggest lever).** The JD names Claude Code/Cursor/Codex. If true, add `AI Tooling: Claude Code, Cursor` to Technical Skills - this is a named-requirement keyword currently scoring zero. See keyword-gaps.md.
2. **"Agent framework" as a literal phrase** appears in the JD but not the resume; "n8n workflow" is the honest nearest hit. If you have LangChain/LangGraph or similar experience not in the masters, record and surface it.
3. **Experience section order is relevance-first, not strictly chronological** (Vault AI Jun-Dec 2025 above Northeastern Jan-Jun 2026). ATS parsers do not penalize this, but some compute "most recent title" from position #1 - here that favorably reads "Software Developer, Vault AI." Keep as-is for this posting; see hiring-manager-scan.md for the human-reader tradeoff.

---

## Score Threshold Interpretation

- **85+:** Ready for external scanner verification + submission
- **70–84:** Iterate on Stage 3 (tailoring) with specific recommendations above
- **<70:** Re-run Stage 2 (gap analysis) — gap may be deeper than tailoring can fix

**This resume: 85 - ready to submit once the Claude Code/Cursor decision (improvement #1) is made.**

## LLM-Tell Scrub Report

- No em dashes, curly quotes, or non-breaking spaces in tailored-resume.md or resume.tex (en dashes only in LaTeX date ranges, which is allowed).
- Master phrases scrubbed during tailoring: "Architected" → "Built"; "Engineered... Agent that orchestrates" → "Shipped... agent that runs"; "n8n orchestrating" → "n8n workflow chaining"; "ensuring enterprise-grade data privacy" (vague) → dropped; "Boosted" → "Cut query latency"; "Lifted" → "Raised".
- No "leveraged", "robust", "seamless", "utilized", "spearheaded", "passionate", or "results-driven" anywhere.
- Verb variety check: no leading verb repeats within a role; "Cut" appears twice across different roles (acceptable).
