# Hi, I'm Elena 👋

### Applied AI Engineer with deep legal-domain expertise

I build applied AI systems that combine LLMs with deterministic application logic, retrieval, APIs, databases, authentication and user-facing products.

My focus is not on model demos in isolation, but on **reliable AI-enabled software**: structured outputs, validation, evidence boundaries, explicit failure handling, security controls and production-ready infrastructure.

Alongside engineering, I have a long-standing legal career focused primarily on supporting businesses. That background gives me a practical perspective on ambiguity, risk, evidence, rules and the consequences of incorrect decisions — particularly useful when building AI systems for high-context and high-responsibility domains.

## What I build

- **Applied AI systems** — controlled LLM workflows, structured generation, deterministic validation and human-review paths
- **RAG and knowledge systems** — private and curated corpora, vector retrieval, source grounding and retrieval boundaries
- **Multimodal products** — text, voice, documents, vision and image generation
- **Backend and full-stack applications** — FastAPI, web interfaces, PostgreSQL, authentication, persistent state and external APIs
- **Production infrastructure** — Docker, CI/CD, Traefik, HTTPS, migrations, health checks, backups and operational runbooks
- **Personal products and technical explorations** — real-use projects for experimenting with provider orchestration, scheduling, personalization, third-party APIs and multimodal UX

## Selected work

### [AI Specification Review & Risk Assistant](https://github.com/eliv1982/ai-spec-review-risk-assistant)
**Applied AI · Structured Outputs · Risk Analysis · FastAPI · Production**

A production-deployed assistant for structured specification review and risk analysis.

The system combines LLM-based analysis with deterministic orchestration, strict output schemas, persistence, controlled fallbacks and export workflows. The emphasis is on keeping model behavior inside explicit application boundaries rather than treating generated output as inherently trustworthy.

---

### [Multimodal Learning Assistant](https://github.com/eliv1982/multimodal-learning-assistant)
**Multimodal AI · RAG · Web + Telegram · OAuth · PostgreSQL · Production**

A multimodal learning product combining chat, private-document retrieval, voice, document processing and cross-channel identity.

The project evolved from a narrower assistant into a production system with authenticated users, private data boundaries, persistent services and both web and Telegram interfaces.

---

### [Vibe Order Infrastructure](https://github.com/eliv1982/vibe-order-infra)
**Backend · PostgreSQL · Migrations · Security · CI/CD · Infrastructure**

A backend and infrastructure project focused on reliable application architecture rather than model interaction.

It demonstrates database lifecycle management, migrations, validation, security boundaries, deployment design and automated verification — the engineering layer that AI-enabled products still need underneath the AI.

---

### [Plain English](https://github.com/eliv1982/plain-english)
**AI Product · Voice · Memory · n8n Automation · Web + Telegram · Production**

An actively developed personal product for practical English learning.

It combines conversational and voice interaction, persistent learning state, mistake-pattern memory and **n8n-powered automation workflows** across web and Telegram interfaces. The project uses n8n as part of the application workflow and integration layer rather than as a standalone demo.

The production baseline is stable while new capabilities continue to be added iteratively.

---

### [Site Insight AI](https://github.com/eliv1982/site-insight-ai)
**Full Stack · Structured AI · External Data · SSRF-Aware Fetching**

A compact full-stack application for turning website content into structured AI-generated insight.

Its main engineering focus is controlled external-data ingestion: bounded fetching, URL and network safety, structured model output and predictable processing limits.

---

### [Business Intake & Triage Assistant](https://github.com/eliv1982/business-intake-triage-assistant)
**Applied AI · Deterministic Routing · Human Review · FastAPI · Production**

A business-intake system in which the LLM interprets incoming requests, while deterministic application logic retains control over routing, clarification, escalation and safe failure.

The project demonstrates a reusable pattern I use across applied AI work:

**LLM proposes → application validates → deterministic logic decides what happens next.**

## Legal AI & domain projects

My legal background lets me work on a class of AI problems where domain boundaries, source quality and the cost of unsupported conclusions matter as much as model capability.

These projects are not positioned as substitutes for professional legal analysis. They are engineering case studies in applying AI to complex, evidence-sensitive legal workflows.

### [RAG Assistant for Independent Guarantees](https://github.com/eliv1982/rag-assistant-independent-guarantees)
**Legal RAG · Curated Corpus · Source Grounding · Russian Law**

A retrieval-based assistant built around a curated corpus of Russian legislation, regulatory materials and court guidance relating to independent guarantees.

The project focuses on retrieval quality, source attribution, corpus boundaries and grounded answers rather than unrestricted legal generation.

**Corpus snapshot:** materials were collected and verified as of **6 October 2026**. The repository is a portfolio case study and is not presented as a continuously updated legal reference.

---

### [Court Decision Extractor](https://github.com/eliv1982/court-decision-extractor)
**Legal NLP · Structured Extraction · Documents · Validation**

A document-processing project for extracting structured information from court decisions.

Its focus is turning long, inconsistently formatted legal texts into predictable structured data while preserving the distinction between extracted facts and generated interpretation.

---

### [Telegram Legal Document Review Assistant](https://github.com/eliv1982/telegram-legal-doc-review-assistant)
**Document AI · Telegram · Legal Review · Controlled Analysis**

A document-review assistant for working with uploaded legal materials through a conversational interface.

The project explores how document parsing, structured analysis and explicit review boundaries can be combined in a practical legal workflow without presenting model output as authoritative legal advice.

## Personal products & technical explorations

I also build personal products to explore technologies and interaction patterns outside formal portfolio cases.

These projects are intentionally practical: they are used to test multimodal UX, external providers, scheduling, personalization, state management and operational reliability under real conditions.

### [Weather Teller](https://github.com/eliv1982/weather-teller-bot)
**External APIs · Provider Reconciliation · Timezones · Alerts · Production**

A weather assistant that combines deterministic weather data with an AI interpretation layer.

What started as a simple API exercise evolved into a reliability-focused product involving multiple data providers, discrepancies between forecast and observed conditions, timezone and DST handling, scheduled alerts, concurrency controls and production operation.

---

### [Rise & Shine](https://github.com/eliv1982/rise-and-shine-bot)
**Generative AI · Images · Voice · Scheduling · PostgreSQL · Production**

A personalized content-delivery product combining generated text, images and voice with scheduled delivery.

The engineering work includes multimodal generation, provider abstraction, scheduling semantics, quotas, persistence and failure handling for unattended delivery workflows.

---

### [MoodMuse](https://github.com/eliv1982/moodmuse-bot)
**Image Generation · Voice · Personalization · Bilingual UX**

A smaller generative product focused on visual content, captions, voice and personalized interaction.

I use it as a compact environment for experimenting with image-generation workflows, provider abstraction and multimodal product UX without the architectural weight of a larger application.

## Engineering approach

I use AI-assisted development extensively, but I treat AI tools as part of the engineering workflow rather than as autonomous decision-makers.

My typical process is:

**define the problem → specify constraints and acceptance criteria → design → implement → test → independently review → verify → decide**

A few principles recur across my projects:

- **Deterministic control around non-deterministic models.** LLMs can interpret, classify or propose; application logic controls what is accepted and what happens next.
- **Explicit boundaries.** Authentication, data ownership, retrieval scope, external network access and failure behavior are designed deliberately rather than left implicit.
- **Verification over confidence.** Tests, CI, smoke checks, independent reviews and production evidence matter more than whether an implementation looks plausible.
- **Independent AI review.** I often use different models or tools for implementation and audit so that the same system is not effectively reviewing its own assumptions.
- **Human ownership of trade-offs.** Architecture, scope, security decisions, acceptance criteria and final approval remain mine.
- **Iterative hardening.** Many projects start small, then become more rigorous as real usage exposes assumptions, edge cases and operational constraints.

For me, AI-assisted engineering is most useful when it increases the speed of exploration **without lowering the standard of evidence required before something is accepted as correct**.

## Tech stack

I prefer choosing tools around the problem rather than building around a fixed stack, but these recur across my projects:

**Languages & backend**  
Python · FastAPI · Pydantic · REST APIs · asynchronous workflows

**AI & retrieval**  
OpenAI APIs · Anthropic models · structured outputs · embeddings · RAG · vector search · multimodal text / voice / vision / image workflows

**Data & state**  
PostgreSQL · SQLite · Qdrant · migrations · persistent application state

**Interfaces & integrations**  
Web applications · Telegram bots · OAuth · external APIs · n8n workflow automation

**Frontend**  
React · Vite · HTML / CSS / JavaScript

**Infrastructure & delivery**  
Docker · Docker Compose · Linux · Traefik · HTTPS · GitHub Actions · CI/CD · health checks · backups · deployment and rollback runbooks

**Engineering workflow**  
Git · GitHub · automated testing · security review · independent AI-assisted code and architecture review

## Current interests

I am especially interested in problems where AI capability alone is not enough and the surrounding system has to provide reliability, context and control.

Current areas I keep returning to include:

- reliable patterns for combining LLM reasoning with deterministic software;
- RAG systems with meaningful source and ownership boundaries;
- multimodal interaction across text, documents, voice, vision and generated media;
- long-lived AI products with persistent identity, memory and state;
- practical Legal AI where traceability and evidence matter;
- using real-world product behavior to discover assumptions that tests and prototypes miss.

## Beyond the portfolio

Most repositories here began with one of three things: a real problem, a technical question I wanted to answer, or simple curiosity.

I tend to learn by building something small enough to understand, then making it increasingly less forgiving: adding real users, persistent data, external providers, deployment, failure cases and independent review.

That progression — from **“can this work?”** to **“under what conditions can I trust it to work?”** — is probably the common thread across the portfolio.

## Find your way around

If you are new to the profile, the six projects in **Selected work** are the best place to start.

For domain-specific work, see **Legal AI & domain projects**.  
For smaller real-use products and technology experiments, see **Personal products & technical explorations**.

Individual repositories contain their own architecture notes, setup instructions, tests and project-specific documentation.

## Connect

[Personal website](https://elivcloud.org) · [LinkedIn](https://www.linkedin.com/in/elena-shlenskova-9609b7133/) · [Telegram](https://t.me/elena_shlenskova)
