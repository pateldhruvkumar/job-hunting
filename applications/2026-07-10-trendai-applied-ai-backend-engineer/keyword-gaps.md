# Keyword Gaps — TrendAI (Trend Micro) / Applied AI Backend Engineer

> Keywords from the JD that are NOT backed by your master `database/*.md` files.
> These were NOT silently inserted into the tailored resume.

## Real Gaps

### AI coding assistants (Claude Code, Cursor, GitHub Copilot)
**JD context:** "AI Mastery: Proven experience using AI coding assistants to explore multiple implementation approaches in parallel and accelerate the SDLC." (also a core, repeated theme)
**Status:** Your database shows you *build* AI systems (agents, RAG, fine-tuning) but never states you *use* AI coding assistants day-to-day. This is arguably the single most-emphasized requirement in the JD.

**Three options:**
1. **Address in cover letter** — frame your AI-first build experience and note fluency with AI-assisted development. (Done in `cover-letter.md`, kept honest and non-specific.)
2. **Add to Skills / master** — if you genuinely use Claude Code / Cursor / Copilot, add "AI-assisted development (Claude Code, Cursor, Copilot)" to `master-experience.md` or the Skills row and I will re-tailor. **This is very likely true for you — worth confirming.**
3. **Acknowledge gap** — leave it; your applied-AI build depth partly compensates, but a named-tool line would materially strengthen the match.

### Docker / containers / containerized workflows
**JD context:** "Cloud & Containers: Experience or strong interest in ... Docker, and containerized workflows."
**Status:** Not present in any database file. JD accepts "strong interest," so this is a soft gap.

**Three options:**
1. Address in cover letter as "ramping on Docker / containerized workflows."
2. Add to Skills as `Familiar with: Docker` — only if true.
3. Acknowledge gap — not a knockout given the "or strong interest" wording.

### CI/CD pipelines (GitHub Actions)
**JD context:** "Infrastructure & DevOps: Write non-application code, including ... CI/CD pipelines (GitHub Actions)."
**Status:** You have a documented Git feature-branch / pull-request workflow (Vault AI, 79 commits) but no explicit CI/CD or GitHub Actions.

**Three options:**
1. Add to Skills as `Familiar with: GitHub Actions` — only if true.
2. Address in cover letter alongside your PR-based workflow.
3. Acknowledge gap.

### Infrastructure as Code (IaC)
**JD context:** "Write non-application code, including Infrastructure as Code (IaC)..."
**Status:** Not present. Your AWS serverless ETL is close in spirit but is not described as IaC (Terraform/CloudFormation/CDK).
**Three options:** learn/add if true; address as adjacent to your AWS serverless work; or acknowledge gap.

### Go / Java (and JUnit / Go testing libraries)
**JD context:** "one or more backend languages such as Go, Java, JavaScript, or Python."
**Status:** You have Python and JavaScript, which satisfy the "one or more" requirement. Go and Java are NOT in your database.
**Decision:** Not a real gap — Python + JS meet the bar. JUnit / Go test libraries left off; your Vitest + pytest testing (see Loose Matches) covers "Python-based frameworks."

### Azure
**JD context:** "cloud-native application development (AWS/Azure)."
**Status:** Only AWS is backed (heavily). Azure not present.
**Decision:** AWS alone satisfies "AWS/Azure." No action needed.

---

## Loose Matches (already used — verify comfort level)

### Automated testing / Python-based frameworks
**Closest match:** Seaweed platform project — "roughly 210 tests across 25 Vitest and React Testing Library files ... plus 5 pytest suites for the FastAPI backend."
**Note:** Real and strong, but lives on the *Software Developer* variant of the seaweed project, not the AI Engineer variant used in this resume. If you want the testing signal on the resume, I can swap in that bullet. Currently surfaced only implicitly.

### Monitoring / observability
**Closest match:** Dots N Key — "real-time monitoring dashboards ... catching and resolving production incidents." Used in resume. Good match for JD's "integrated monitoring and observability."

### High availability / on-call rotations
**Closest match:** Dots N Key — "Maintained 99.9% system uptime ... resolving production incidents before end-user impact." Used in resume. Reasonable proxy for the on-call/HA expectation.

### Vector/Graph DBs
**Closest match:** Vault AI RAG pipelines + seaweed embeddings (vector). **Vector = strong match; Graph DBs = no match.** JD says "Vector/Graph DBs" (or), so vector satisfies it.

---

## Master Resume Updates Suggested

- **Highest priority:** if you use Claude Code / Cursor / Copilot, add an explicit line to `master-experience.md`. It directly answers the JD's most-emphasized requirement.
- Add Docker / GitHub Actions / IaC to the master **only if true** — do not invent.
