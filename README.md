# Hi, I'm Elena 👋

### Applied AI Engineer with legal-domain expertise

I build LLM-backed applications that combine model capabilities with deterministic application logic, retrieval, APIs, databases, authentication, external integrations and user-facing products.

I care most about the engineering around the model: typed contracts, explicit failure behavior, retrieval and ownership boundaries, deterministic checks, safe fallbacks and deployable software.

Alongside engineering, I have a long-standing legal career focused primarily on supporting businesses. That experience gives me a practical perspective on ambiguity, evidence, risk, rules and the consequences of unsupported conclusions.

## Selected work

### [AI Specification Review & Risk Assistant](https://github.com/eliv1982/ai-spec-review-risk-assistant)
**Applied AI · Structured Outputs · Backend QC · FastAPI · Self-hosted**

A self-hosted assistant for structured specification review and risk analysis, deployed behind a Basic Auth perimeter.

Model drafts are converted into typed final outputs through backend-owned QC, closed reason codes, persistence and safe fallbacks rather than being accepted directly as final answers.

**Evidence:** [review contract](https://github.com/eliv1982/ai-spec-review-risk-assistant/blob/main/docs/REVIEW_SCHEMA.md) · [CI](https://github.com/eliv1982/ai-spec-review-risk-assistant/actions)

---

### [Multimodal Learning Assistant](https://github.com/eliv1982/multimodal-learning-assistant)
**Private RAG · Multimodal Telegram · OAuth · PostgreSQL · Self-hosted**

An invite-only learning system with per-user private documents, retrieval ownership boundaries, GitHub OAuth / Telegram account linking and persistent PostgreSQL state.

RAG, voice, vision and image workflows currently live in Telegram; the current web chat is text-only.

**Evidence:** [repository](https://github.com/eliv1982/multimodal-learning-assistant) · [CI](https://github.com/eliv1982/multimodal-learning-assistant/actions)

---

### [Site Insight AI](https://github.com/eliv1982/site-insight-ai)
**React · FastAPI · Structured AI · SSRF-aware Fetching**

A compact full-stack application for analyzing a single public web page.

Its fetch boundary validates scheme and port, rejects non-global DNS results, revalidates redirects, bounds decompression and returns strictly validated structured output. Residual limitations are documented rather than hidden.

**Evidence:** [fetch / analysis boundary](https://github.com/eliv1982/site-insight-ai/blob/main/app/services/analyzer.py) · [CI](https://github.com/eliv1982/site-insight-ai/actions)

---

### [Telegram Legal Document Review Assistant](https://github.com/eliv1982/telegram-legal-doc-review-assistant)
**Document AI · Verifiable Facts · Structured Review · CI**

A legal-document review assistant designed to keep code-verifiable facts separate from model interpretation.

Quotes count as evidence only when they occur verbatim in the extracted source text, while checksum results are handled deterministically rather than being delegated to the model.

The repository uses synthetic demo assets and locked-dependency CI so the engineering behavior can be reviewed without exposing real documents.

**Evidence:** [repository and rule table](https://github.com/eliv1982/telegram-legal-doc-review-assistant) · [CI](https://github.com/eliv1982/telegram-legal-doc-review-assistant/actions)

---

### [Plain English](https://github.com/eliv1982/plain-english)
**Voice · Memory · n8n · Web + Telegram · Personal Product**

An actively developed English-learning product that grew from a study project.

It combines conversational and voice interaction, persistent learning state, mistake-pattern memory and a nightly n8n workflow across web and Telegram interfaces.

The product continues to be hardened iteratively rather than being presented as a finished platform.

**Evidence:** [architecture and scope decisions](https://github.com/eliv1982/plain-english/blob/main/docs/architecture-scope.md)

---

### [Vibe Order Infrastructure](https://github.com/eliv1982/vibe-order-infra)
**PostgreSQL · Migrations · Least Privilege · CI**

Originally an infrastructure assignment, later hardened into a database-lifecycle and deployment case.

The project covers three-role PostgreSQL least privilege, fail-closed Alembic migrations, legacy-database adoption and migration rehearsal. Its live deployment was intentionally decommissioned after verification; continuous deployment is not implemented.

**Evidence:** [repository](https://github.com/eliv1982/vibe-order-infra) · [CI](https://github.com/eliv1982/vibe-order-infra/actions)

## Additional applied AI case

### [Business Intake & Triage Assistant](https://github.com/eliv1982/business-intake-triage-assistant)

A feature-frozen demo on synthetic data where the LLM interprets incoming requests while deterministic application logic controls human review, clarification, routing and safe failure.

Its decision layer is a compact example of the pattern:

**LLM proposes → application validates → deterministic logic decides what happens next.**

**Evidence:** [decision service](https://github.com/eliv1982/business-intake-triage-assistant/blob/main/app/services/decision_service.py) · [CI](https://github.com/eliv1982/business-intake-triage-assistant/actions)

## Legal AI & domain work

My legal background is most useful when the system must distinguish between what the evidence supports, what the corpus contains and what the model merely infers.

### [RAG Assistant for Independent Guarantees](https://github.com/eliv1982/rag-assistant-independent-guarantees)
**Legal RAG · Curated Corpus · Source Boundaries · Russian Law**

A legal-RAG case built around a curated corpus of legislation, regulatory materials and court guidance concerning independent guarantees.

The interesting part is not unrestricted legal generation, but layered sources, scope boundaries, attribution and the distinction between **“not found in this corpus”** and **“not part of the law.”**

**Corpus note:** this is a curated snapshot. Exact retrieval dates and consolidated-edition metadata were not preserved, so the repository does **not** claim that the corpus is current as of a specific date. Current law should be verified against official sources.

### [Court Decision Extractor](https://github.com/eliv1982/court-decision-extractor)

A smaller CLI experiment in structured extraction from court decisions. Structured output validates the shape of the response, not the factual correctness of model-generated summaries or findings.

## Personal products & technical explorations

Smaller products give me a place to test APIs, multimodal interaction and reliability under real use without pretending that every experiment is a platform.

- **[Weather Teller](https://github.com/eliv1982/weather-teller-bot)** — weather-provider comparison, PostgreSQL state, alerts and timezone / DST handling; currently a beta rather than a production service.
- **[Rise & Shine](https://github.com/eliv1982/rise-and-shine-bot)** — scheduled text / image / voice delivery with a durable delivery ledger, atomic claims and explicit at-least-once semantics.
- **[MoodMuse](https://github.com/eliv1982/moodmuse-bot)** — a smaller bilingual playground for image generation, voice and personalized multimodal UX.

## Engineering approach

I use AI-assisted development extensively, but I evaluate the result as software rather than treating the tool output as evidence of correctness.

Three patterns recur across the portfolio:

- **Model output stays inside application boundaries.** In specification review and intake triage, typed contracts and deterministic decision logic decide what becomes an application action.
- **Security boundaries are explicit.** Site Insight validates external network access before content reaches the model, and its remaining DNS-rebinding limitation is documented rather than silently ignored.
- **Reliability claims are deliberately narrow.** Rise & Shine records delivery attempts durably and explicitly documents at-least-once behavior instead of claiming exactly-once delivery.

Independent AI review is part of my workflow, but architecture, scope, trade-offs, acceptance criteria and final approval remain human-controlled.

My usual loop is:

**define → specify → build → test → independently review → verify → decide**

## Tech stack

**Application engineering:** Python · FastAPI · Pydantic · PostgreSQL · SQLite · React · TypeScript · Vite

**AI / retrieval:** OpenAI APIs · Anthropic models · structured outputs · embeddings · RAG · ChromaDB · Qdrant · LangChain where appropriate · text / voice / vision / image workflows

**Integrations:** Telegram · OAuth · external APIs · n8n

**Delivery:** Docker · Docker Compose · Linux · Traefik · HTTPS · GitHub Actions · CI · scripted / manual deployment · backups and runbooks

## Connect

[Personal website](https://elivcloud.org) · [LinkedIn](https://www.linkedin.com/in/elena-shlenskova-9609b7133/) · [Telegram](https://t.me/elena_shlenskova)
