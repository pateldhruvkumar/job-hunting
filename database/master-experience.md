# Master Experience

> Canonical work-experience record. Use this file as the source of truth when tailoring resumes for specific job applications. Companion files for technical skills, education, and projects will live alongside it.

---

## Operations Data Assistant — Northeastern University | Jan 2026 – Jun 2026

- Optimized Power BI dashboards by refactoring DAX measures and calculated columns, reducing report refresh time by 13%.
- Managed a student records database of 1,000+ active students, maintaining data accuracy and integrity to support operations reporting and daily workflows.
- Diagnosed and rewrote an inefficient cost-calculation query in the operations database, correcting pricing logic and reducing university order spend by thousands of dollars annually.

---

## Software Developer — Vault AI | Jun 2025 – Dec 2025

- Architected an AI-powered client intake portal for private credit firms, enabling natural-language analytics on financial data and automated extraction from unstructured PDFs, built on Supabase and serverless Edge Functions for real-time processing.
- Engineered an autonomous Due Diligence Agent that orchestrates multi-source web research to synthesize credit risk and legal compliance into production-ready PDF reports.
- Designed a Multi-Company Financial Comparison Agent to benchmark fiscal performance across entities, reducing manual comparison effort by 60%.
- Built secure RAG pipelines over 100+ confidential documents with vector retrieval, ensuring enterprise-grade data privacy and reliable grounding for complex inquiries.
- Fine-tuned Llama models with QLoRA on domain-specific terminology, improving answer accuracy by 15% on internal evaluations.
- Engineered a unified text-to-speech playback controller in React that streams and cancels audio across 4 providers (browser SpeechSynthesis, OpenAI, ElevenLabs, and local Piper/ONNX in-browser inference), using MediaSource Extensions and AbortController for chunked streaming and clean teardown.
- Designed an event-driven synchronization layer using browser CustomEvents (STOP_TTS_PLAYBACK, TTS_PLAYBACK_STARTED/ENDED) to coordinate playback state across independent chat components and guarantee cleanup on unmount, eliminating overlapping-audio bugs.
- Built a runtime theming system with CSS custom properties and a React context, letting users switch light/dark themes and custom logos instantly without a page reload, and removed the screen-flicker that occurred on theme change.
- Implemented a global modal-state mechanism that broadcasts open/close events so dropdown menus (agent-type selector, saved prompts, slash commands) close correctly and stop capturing input while a modal is open.
- Rebuilt core chat components (message bubbles and inline message editing) with an auto-resizing textarea and dynamic message alignment, improving the in-place editing experience and readability.
- Added per-response PDF export with jsPDF, enabling users to download any individual chat answer as a formatted document.
- Shipped per-workspace AI model selection with a specialist-model dropdown and tooltips, and fixed a race condition that left text generation running when a user switched models mid-stream.
- Extended Node/Express endpoints and system-settings models to persist appearance and TTS configuration consumed by the React client, working across the full stack.
- Improved workspace navigation by adding search-by-workspace, refining sidebar layout and scroll behavior, and reworking thread option menus for consistency.
- Implemented client-side password validation and refined the multi-user authentication and account-management modals.
- Optimized responsive layout and accessibility across chat, settings, and onboarding views (input alignment, scroll containers, dimension fixes) to support varied screen sizes.
- Collaborated on a 3-service monorepo (React/Vite frontend, Node/Express API, document collector) alongside a 7-developer team, contributing 79 commits through a Git feature-branch and pull-request workflow.

---

## Software Developer — Dots N Key, Surat, India | Dec 2022 – Jul 2024

- Led backend performance, cloud infrastructure, and full-stack optimization for a high-traffic retail POS platform running production workloads.
- Boosted query performance by 60% on the SONAR POS platform by leading the full MySQL to AWS RDS migration, eliminating single-point-of-failure risk and unlocking production-grade scalability for high-traffic retail operations.
- Maintained 99.9% system uptime by deploying cloud infrastructure on AWS EC2 and S3 with real-time monitoring dashboards, catching and resolving production incidents before end-user impact.
- Lifted web application performance by 35% and trimmed data-handling overhead by 25% through tuned React.js rendering, refactored Node.js logic, and optimized stored procedures across the full stack.

---

## Software Developer — Unistar Softech Private Ltd., Bardoli, India | May 2022 – Nov 2022

- Engineered full-stack dashboards, backend services, and role-based access control for multi-user enterprise operations.
- Delivered real-time operational visibility by building 14 interactive PHP/HTML/MySQL dashboards for 12+ stakeholders, replacing spreadsheet-based reporting and cutting report turnaround by 40%.
- Sped up backend processing by 30% by refactoring Node.js scripts and tuning database queries, cutting report generation time and clearing delays in business-critical data delivery.
- Hardened application security by implementing Role-Based Access Control (RBAC) with 21 role tiers and integrating 45+ third-party task-orchestration APIs, cutting cross-team handoff delays by 23% in multi-user environments.
