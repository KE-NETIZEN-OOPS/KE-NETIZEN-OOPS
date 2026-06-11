<h1 align="center">Hi, I'm Abed Kamau 👋</h1>

<p align="center">
  <b>Software & AI engineer</b> — I build multi-agent AI systems, trading & market-data infrastructure, and multi-tenant SaaS platforms.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
</p>

---

### What I do

I'm a full-stack engineer who works across the AI, fintech, and SaaS stacks. I like
turning fuzzy problems into small, well-tested systems with clear boundaries — the
kind of code you can hand to a teammate and they immediately know how to use, extend,
and trust. Most of what I ship runs in CI, is tested offline without secrets, and
ships with real docs.

- 🤖 **AI engineering** — multi-agent orchestration, RAG, LLM eval & regression testing, Model Context Protocol (MCP) servers, working against the Claude and OpenAI APIs.
- 📈 **Trading & market data** — event-driven backtesting, real-time market dashboards, on-chain wallet analytics, rate-limiting and queueing infra.
- 🧱 **SaaS & platforms** — multi-tenant architecture with row-level security, auth, RBAC, and audit logging on Next.js + Supabase + Postgres.

---

### 🛠️ Tech I work with

| Area | Tools |
|------|-------|
| **Languages** | TypeScript · Python · Rust · Go · SQL |
| **AI / LLM** | Claude API · OpenAI · multi-agent orchestration · RAG (BM25 + vector + RRF) · MCP · LLM-as-judge & eval harnesses |
| **Backend** | Node.js · FastAPI · Next.js (App Router) · REST · WebSockets · gRPC |
| **Data / infra** | PostgreSQL · pgvector · SQLite · bbolt · Prometheus · Docker |
| **Web / SaaS** | Next.js · Supabase · Row-Level Security · multi-tenancy · Stripe |
| **Quant / on-chain** | backtesting engines · OHLCV aggregation · EVM/ERC-20 analytics · PnL accounting |
| **Quality** | Vitest · Pytest · `cargo test` · `go test -race` · GitHub Actions CI · Zod / Pydantic typing |

---

### 🚀 Featured projects

A portfolio of focused, production-quality systems — each is independently tested, runs
in CI, and is documented with an architecture diagram. They're built to be **testable
offline** (network, keys, and databases sit behind interfaces with deterministic mocks).

#### AI engineering
| Project | Stack | What it is |
|---------|-------|------------|
| [**agent-foundry**](https://github.com/KE-NETIZEN-OOPS/agent-foundry) | TypeScript | Provider-agnostic framework for multi-agent systems: typed tools, an agentic loop, planner→worker→critic orchestration, and a built-in eval harness. |
| [**ragforge**](https://github.com/KE-NETIZEN-OOPS/ragforge) | Python | Production-grade RAG core — hybrid retrieval (BM25 + vector + RRF), reranking, citation-aware answers, an eval suite, and a FastAPI service. |
| [**mcp-toolkit**](https://github.com/KE-NETIZEN-OOPS/mcp-toolkit) | TypeScript | A suite of Model Context Protocol servers (SQLite explorer, web research, scheduler) on a shared, Zod-typed mini-framework. |
| [**promptproof**](https://github.com/KE-NETIZEN-OOPS/promptproof) | Python | LLM regression-testing CLI: YAML specs, regex / semantic / LLM-judge assertions, CI-friendly exit codes, and HTML reports. |

#### Trading, quant & on-chain
| Project | Stack | What it is |
|---------|-------|------------|
| [**tickforge**](https://github.com/KE-NETIZEN-OOPS/tickforge) | Rust | Deterministic, event-driven backtesting engine with a `Strategy` trait, fee/slippage models, metrics, and criterion benchmarks. |
| [**pulseboard**](https://github.com/KE-NETIZEN-OOPS/pulseboard) | TypeScript | Real-time market dashboard — WebSocket trade ingestion, server-side OHLCV candle aggregation, a pluggable alert engine, and live charts. |
| [**chainlens**](https://github.com/KE-NETIZEN-OOPS/chainlens) | Python | On-chain EVM wallet analytics: ERC-20 ingestion behind a provider interface, average-cost PnL, address clustering, and an alert engine. |

#### Systems & infrastructure
| Project | Stack | What it is |
|---------|-------|------------|
| [**roomcast**](https://github.com/KE-NETIZEN-OOPS/roomcast) | Go · TS | Self-hostable real-time collaboration engine: rooms, presence, and a conflict-free (LWW-CRDT) shared-state core over WebSockets, with a pluggable broker for multi-node scale and a typed TypeScript client SDK. |
| [**conveyor**](https://github.com/KE-NETIZEN-OOPS/conveyor) | Go | Race-tested job queue: worker pool, exponential-backoff retries, dead-letter queue, REST API, Prometheus metrics, in-memory or bbolt backend. |
| [**quotaguard**](https://github.com/KE-NETIZEN-OOPS/quotaguard) | Rust | Composable rate-limiting library — token bucket, sliding window, and GCRA behind one trait, with an injectable clock for deterministic tests. |
| [**tenantkit**](https://github.com/KE-NETIZEN-OOPS/tenantkit) | TypeScript | Multi-tenant SaaS starter: a pure, tested domain core (orgs, RBAC, expiring invites, audit log) plus Next.js and Postgres row-level-security policies. |

#### Automation & data tooling
| Project | Stack | What it is |
|---------|-------|------------|
| [**job-hunt-copilot**](https://github.com/KE-NETIZEN-OOPS/job-hunt-copilot) | Python | AI job-search copilot: ingests postings from public feeds, scores fit against your resume (lexical or LLM), tracks applications, and drafts tailored cover letters. |
| [**leadforge**](https://github.com/KE-NETIZEN-OOPS/leadforge) | TypeScript | Lead qualification & enrichment engine over data you own — normalize, dedupe, enrich (pluggable provider), and score into A/B/C tiers. Not a scraper. |
| [**x-signal**](https://github.com/KE-NETIZEN-OOPS/x-signal) | Go | Rate-limited ETL & signal pipeline over the official X API v2 (with a public RSS fallback): normalize, store, and aggregate post signals, ToS-respecting. |

#### Security
| Project | Stack | What it is |
|---------|-------|------------|
| [**lucid-scanner**](https://github.com/KE-NETIZEN-OOPS/lucid-scanner) | Python | Stack-aware web security auditor (WordPress / Next.js / Vercel / Rails-Devise) producing prioritized, remediation-focused reports. Authorized-use only. |

> Beyond these, my profile includes earlier work across web apps, automation/integrations
> (e.g. a [Wix ↔ HubSpot sync](https://github.com/KE-NETIZEN-OOPS/wix-hubspot-integration)),
> dashboards, and trading tooling. Browse the [repositories tab](https://github.com/KE-NETIZEN-OOPS?tab=repositories) for the full picture.

---

### 📊 GitHub

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=KE-NETIZEN-OOPS&show_icons=true&hide_border=true&theme=default" alt="GitHub stats" height="160" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=KE-NETIZEN-OOPS&layout=compact&hide_border=true&langs_count=8" alt="Top languages" height="160" />
</p>

---

<p align="center"><i>Open to interesting work in AI engineering, fintech infrastructure, and SaaS platforms.</i></p>
