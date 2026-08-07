# Danilo Cordeiro

**Senior Software Engineer** · Backend & Distributed Systems

Building distributed systems in Java, Kotlin, and Go — ledgers, reconciliation, event-driven architecture. 11+ years across fintech, healthcare, and retail forecasting (Arcotech, Conexa Saúde, Grupo Boticário, Inventa). The two projects below are fully-documented reference systems: real architecture decisions, trade-offs written down, tests that would catch a regression.

## Distributed Ledger System

A double-entry ledger built as four coordinated services, not four isolated demos — each one absorbs a specific hard problem (idempotency, event streaming, CQRS, bank reconciliation).

- **[ledger-core](https://github.com/dev-danilocordeiro/ledger-core)** — Kotlin/Spring. Idempotent posting, pessimistic locking under a global lock order, transactional outbox, zero-sum invariants enforced by the database.
- **[ledger-gateway](https://github.com/dev-danilocordeiro/ledger-gateway)** — Kotlin/WebFlux. OAuth2 resource server, distributed rate limiting, circuit breakers — the only service exposed to the outside world.
- **[ledger-query](https://github.com/dev-danilocordeiro/ledger-query)** — Go. CQRS read side: event-driven cache invalidation, cursor pagination, a reconciliation job that alerts on drift instead of silently correcting it.
- **[ledger-recon](https://github.com/dev-danilocordeiro/ledger-recon)** — Go. Reconciles CNAB240 bank return files against the ledger's event stream; worker pool with backpressure and a measured throughput report.

## URL Shortener System

A control plane / data plane split — link creation and management (Java) is a separate deployable from redirect resolution (Go), so an outage in one never takes down the other.

- **[shortlink-api](https://github.com/dev-danilocordeiro/shortlink-api)** — Java/Spring Boot. Control plane: Snowflake id generation, transactional outbox, Redis-backed rate limiting.
- **[shortlink-edge](https://github.com/dev-danilocordeiro/shortlink-edge)** — Go. Data plane: high-volume redirect resolution and real-time click analytics.

## Currently exploring

AI-augmented engineering workflows — MCP tooling and code-review agents, so engineering time goes where judgment actually matters.

## Stack

| Category | Technologies |
|---|---|
| Languages | Java, Kotlin, Go, TypeScript, Python |
| Frameworks | Spring Boot, Spring WebFlux, Micronaut, NestJS |
| Data & Messaging | PostgreSQL, Oracle, MongoDB, MySQL, Redis, Kafka, gRPC |
| Infra & Practice | Kubernetes, Docker, AWS, GCP, DDD, Hexagonal, TDD |

![GitHub stats](https://github-readme-stats.vercel.app/api?username=dev-danilocordeiro&theme=dark&hide_border=true&include_all_commits=true&count_private=true)

**Contact:** [email](mailto:danilocordeiroti@gmail.com) · [LinkedIn](https://www.linkedin.com/in/danilocordeirodev) · [portfolio](https://dev-danilocordeiro.github.io)
