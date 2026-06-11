# Abed Kamau

**Software & AI Engineer** — I design and ship production systems across AI, fintech, and SaaS, and own them end to end: architecture, implementation, containerization, deployment, and ongoing maintenance.

My work spans multi-agent AI frameworks, real-time and distributed infrastructure, trading and on-chain analytics, and multi-tenant platforms. I optimize for correctness and longevity — small, well-bounded services with explicit interfaces, comprehensive offline test suites, CI on every push, and documentation a teammate can actually use.

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white" alt="AWS" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
</p>

---

## Core competencies

| Domain | Detail |
|--------|--------|
| **AI & LLM systems** | Multi-agent orchestration, RAG, Model Context Protocol (MCP) servers, eval & regression harnesses, agentic tool-calling; Claude and OpenAI APIs |
| **Backend & distributed systems** | Node.js, FastAPI, Next.js, Go; REST, gRPC, WebSockets; CRDTs, job queues, rate limiting, real-time fan-out |
| **Trading & market-data infrastructure** | Event-driven backtesting, real-time OHLCV aggregation, signal/alert engines, market-data ingestion |
| **Blockchain analysis & engineering** | EVM/ERC-20 analytics, wallet clustering & PnL accounting, on-chain arbitrage, DeFi data pipelines |
| **SaaS & multi-tenant platforms** | Next.js + Supabase, Postgres Row-Level Security, RBAC, audit logging, billing integration (Stripe) |
| **Cloud, containers & operations** | AWS, Docker, GitHub Actions CI/CD, Prometheus monitoring; production support, long-running system maintenance and incident remediation |
| **Applications** | Web apps (React/Next.js), Android, command-line tools, third-party integrations (OAuth 2.0) |
| **Security** | Stack-aware web auditing, secret-leak detection, responsible disclosure |
| **Languages** | TypeScript · Python · Rust · Go · SQL |

---

## Engineering standards

Every project below is built to the same bar: external dependencies (LLMs, databases, market feeds, blockchain RPCs, third-party APIs) sit behind interfaces with deterministic mocks, so the full system is **tested offline with no secrets**; CI runs **green on every push**; and each repository ships with an **architecture diagram** and an honest *what-this-is-and-isn't* scope section.

---

## Selected work

### AI engineering
| Project | Stack | Summary |
|---------|-------|---------|
| [**agent-foundry**](https://github.com/KE-NETIZEN-OOPS/agent-foundry) | TypeScript | Provider-agnostic framework for multi-agent systems: typed Zod tools, an agentic tool-calling loop, planner→worker→critic orchestration with a revision loop, and a built-in eval harness. A single `Provider` interface is the only LLM touch-point, so the whole stack runs offline against a mock. |
| [**ragforge**](https://github.com/KE-NETIZEN-OOPS/ragforge) | Python | Production-grade RAG core + FastAPI service: hybrid retrieval (BM25 + vector + Reciprocal Rank Fusion), reranking, citation-aware answers, and an eval suite (recall@k + faithfulness). Optional Postgres/pgvector backend; deterministic no-API-key defaults. |
| [**mcp-toolkit**](https://github.com/KE-NETIZEN-OOPS/mcp-toolkit) | TypeScript | A suite of Model Context Protocol servers on a shared, Zod-typed mini-framework — a read-only SQLite explorer, a web-research server, and a scheduler — with handlers testable without transport or network. |
| [**promptproof**](https://github.com/KE-NETIZEN-OOPS/promptproof) | Python | LLM regression-testing CLI: YAML specs, regex / semantic-similarity / LLM-judge assertions, CI-friendly exit codes, and HTML reports. The model sits behind an interface with a deterministic fake. |

### Trading, quant & on-chain
| Project | Stack | Summary |
|---------|-------|---------|
| [**tickforge**](https://github.com/KE-NETIZEN-OOPS/tickforge) | Rust | Deterministic, event-driven backtesting engine: a `Strategy` trait, configurable fee/slippage models, performance metrics (return, max drawdown), example strategies, and criterion benchmarks. |
| [**pulseboard**](https://github.com/KE-NETIZEN-OOPS/pulseboard) | TypeScript | Real-time market dashboard: WebSocket trade ingestion, server-side OHLCV candle aggregation, and a pluggable alert engine. The feed sits behind an interface, so aggregation logic is unit-tested deterministically. |
| [**chainlens**](https://github.com/KE-NETIZEN-OOPS/chainlens) | Python | Provider-agnostic EVM wallet analytics: ERC-20 ingestion, average-cost realized/unrealized PnL, address-clustering heuristics, and an alert rule engine — all tested over fixtures with no RPC. |

### Systems & infrastructure
| Project | Stack | Summary |
|---------|-------|---------|
| [**roomcast**](https://github.com/KE-NETIZEN-OOPS/roomcast) | Go · TypeScript | Self-hostable real-time collaboration engine: rooms, presence, and a conflict-free (LWW-CRDT) shared-state core over WebSockets, with a pluggable broker for multi-node scale and a typed TypeScript client SDK. Race-detector-clean; CRDT convergence verified across reordered-op permutations. |
| [**conveyor**](https://github.com/KE-NETIZEN-OOPS/conveyor) | Go | Race-tested job queue: priority queue, worker pool with graceful shutdown, exponential-backoff retries, dead-letter queue, REST API, Prometheus metrics, and an in-memory or bbolt backend. |
| [**quotaguard**](https://github.com/KE-NETIZEN-OOPS/quotaguard) | Rust | Composable rate-limiting library: token bucket, sliding window, and GCRA behind one trait, with an injectable clock for deterministic tests. |

### SaaS & platforms
| Project | Stack | Summary |
|---------|-------|---------|
| [**tenantkit**](https://github.com/KE-NETIZEN-OOPS/tenantkit) | TypeScript | Multi-tenant SaaS starter: a pure, tested domain core (organizations, RBAC, expiring invitations, audit log) behind a `TenantStore` interface, plus a Next.js shell and a Postgres Row-Level-Security migration. |

### Automation & data tooling
| Project | Stack | Summary |
|---------|-------|---------|
| [**job-hunt-copilot**](https://github.com/KE-NETIZEN-OOPS/job-hunt-copilot) | Python | AI job-search copilot: public-feed posting ingestion, resume fit-scoring (lexical or LLM), a SQLite application tracker, and tailored cover-letter drafting. |
| [**leadforge**](https://github.com/KE-NETIZEN-OOPS/leadforge) | TypeScript | Lead qualification & enrichment engine over data you own — normalize, dedupe, enrich (pluggable provider), and score into A/B/C tiers. Operates on user-provided data; no scraping. |
| [**x-signal**](https://github.com/KE-NETIZEN-OOPS/x-signal) | Go | Rate-limited ETL & signal pipeline on the official X API v2 with a public RSS fallback: token-bucket limiting, normalization, storage, and signal aggregation — tested entirely against mocks. |

### Security
| Project | Stack | Summary |
|---------|-------|---------|
| [**lucid-scanner**](https://github.com/KE-NETIZEN-OOPS/lucid-scanner) | Python | Stack-aware web security auditor (WordPress / Next.js / Vercel / Rails-Devise): runs only relevant checks and produces prioritized reports with evidence, impact, and a specific fix per finding. Authorized-use only. |

---

## Additional projects

| Project | Stack | Description |
|---------|-------|-------------|
| [tradeflow-dashboard](https://github.com/KE-NETIZEN-OOPS/tradeflow-dashboard) | TypeScript · Postgres | Trading-flow dashboard over a PL/pgSQL backend |
| [titan-watch](https://github.com/KE-NETIZEN-OOPS/titan-watch) | TypeScript | Monitoring / watchlist dashboard |
| [glyph-alpha-panel](https://github.com/KE-NETIZEN-OOPS/glyph-alpha-panel) | TypeScript | Alpha-signal control panel |
| [theperfectgiftbox](https://github.com/KE-NETIZEN-OOPS/theperfectgiftbox) | TypeScript · Postgres | E-commerce storefront |
| [analyzer](https://github.com/KE-NETIZEN-OOPS/analyzer) | Rust · Python | Market / data analyzer |
| [Clubmillies](https://github.com/KE-NETIZEN-OOPS/Clubmillies) | Python | MetaTrader 5 gold-trading bot |
| [simulation_optimizer](https://github.com/KE-NETIZEN-OOPS/simulation_optimizer) | Python | Simulation parameter optimizer |
| [call_forwarder](https://github.com/KE-NETIZEN-OOPS/call_forwarder) | Python | Call-forwarding automation service |
| [wix-hubspot-integration](https://github.com/KE-NETIZEN-OOPS/wix-hubspot-integration) | JavaScript | Bi-directional Wix ↔ HubSpot contact sync with OAuth 2.0 |
| [Vulnerability-scout](https://github.com/KE-NETIZEN-OOPS/Vulnerability-scout) | — | Security-audit tooling |
| [amazing-abed](https://github.com/KE-NETIZEN-OOPS/amazing-abed) | TypeScript · Docker | Automation & tooling monorepo |

---

## GitHub

<p>
  <img src="https://github-readme-stats.vercel.app/api?username=KE-NETIZEN-OOPS&show_icons=true&hide_border=true&count_private=true&theme=transparent" alt="GitHub stats" height="165" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=KE-NETIZEN-OOPS&layout=compact&hide_border=true&langs_count=8&theme=transparent" alt="Top languages" height="165" />
</p>

---

<sub>Available for engagements in AI engineering, fintech infrastructure, and SaaS platforms.</sub>
