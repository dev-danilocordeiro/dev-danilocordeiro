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

**Languages**

![Kotlin](https://img.shields.io/badge/Kotlin-13171E?style=for-the-badge&logo=kotlin&logoColor=7F52FF)
![Java](https://img.shields.io/badge/Java-13171E?style=for-the-badge&logo=openjdk&logoColor=E76F00)
![Go](https://img.shields.io/badge/Go-13171E?style=for-the-badge&logo=go&logoColor=00ADD8)
![TypeScript](https://img.shields.io/badge/TypeScript-13171E?style=for-the-badge&logo=typescript&logoColor=3178C6)
![Python](https://img.shields.io/badge/Python-13171E?style=for-the-badge&logo=python&logoColor=3776AB)

**Frameworks & Runtime**

![Spring](https://img.shields.io/badge/Spring_Boot-13171E?style=for-the-badge&logo=spring&logoColor=6DB33F)
![Micronaut](https://img.shields.io/badge/Micronaut-13171E?style=for-the-badge&logo=micronaut&logoColor=1997F1)
![NestJS](https://img.shields.io/badge/NestJS-13171E?style=for-the-badge&logo=nestjs&logoColor=E0234E)

**Data & Messaging**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13171E?style=for-the-badge&logo=postgresql&logoColor=4169E1)
![Redis](https://img.shields.io/badge/Redis-13171E?style=for-the-badge&logo=redis&logoColor=DC382D)
![Apache Kafka](https://img.shields.io/badge/Kafka-13171E?style=for-the-badge&logo=apachekafka&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-13171E?style=for-the-badge&logo=mongodb&logoColor=47A248)

**Infra & Cloud**

![Docker](https://img.shields.io/badge/Docker-13171E?style=for-the-badge&logo=docker&logoColor=2496ED)
![Kubernetes](https://img.shields.io/badge/Kubernetes-13171E?style=for-the-badge&logo=kubernetes&logoColor=326CE5)
![AWS](https://img.shields.io/badge/AWS-13171E?style=for-the-badge&logo=amazonaws&logoColor=FF9900)
![Google Cloud](https://img.shields.io/badge/GCP-13171E?style=for-the-badge&logo=googlecloud&logoColor=4285F4)

**Practice & Tooling**

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-13171E?style=for-the-badge&logo=githubactions&logoColor=2088FF)
![Prometheus](https://img.shields.io/badge/Prometheus-13171E?style=for-the-badge&logo=prometheus&logoColor=E6522C)
![Grafana](https://img.shields.io/badge/Grafana-13171E?style=for-the-badge&logo=grafana&logoColor=F46800)

![GitHub stats](https://github-readme-stats.vercel.app/api?username=dev-danilocordeiro&theme=dark&hide_border=true&include_all_commits=true&count_private=true)

**Contact:** [email](mailto:danilocordeiro.ti@gmail.com) · [LinkedIn](https://www.linkedin.com/in/danilocordeirodev) · [portfolio](https://dev-danilocordeiro.github.io)

---

<details>
<summary><strong>🇧🇷 Português</strong></summary>

<br>

**Engenheiro de Software Sênior** · Backend & Sistemas Distribuídos

Construo sistemas distribuídos em Java, Kotlin e Go — ledgers, conciliação, arquitetura orientada a eventos. 11+ anos entre fintech, saúde e forecasting de varejo (Arcotech, Conexa Saúde, Grupo Boticário, Inventa). Os dois projetos abaixo são sistemas de referência totalmente documentados: decisões de arquitetura reais, trade-offs registrados, testes que pegariam uma regressão.

#### Sistema de Ledger Distribuído

Um ledger de dupla entrada construído como quatro serviços coordenados, não quatro demos isoladas — cada um absorve um problema difícil específico (idempotência, streaming de eventos, CQRS, conciliação bancária).

- **[ledger-core](https://github.com/dev-danilocordeiro/ledger-core)** — Kotlin/Spring. Lançamento idempotente, locking pessimista sob ordem global de locks, transactional outbox, invariantes de soma-zero garantidas pelo banco.
- **[ledger-gateway](https://github.com/dev-danilocordeiro/ledger-gateway)** — Kotlin/WebFlux. Resource server OAuth2, rate limiting distribuído, circuit breakers — o único serviço exposto ao mundo externo.
- **[ledger-query](https://github.com/dev-danilocordeiro/ledger-query)** — Go. Lado de leitura CQRS: invalidação de cache orientada a eventos, paginação por cursor, um job de conciliação que alerta sobre divergência em vez de corrigir silenciosamente.
- **[ledger-recon](https://github.com/dev-danilocordeiro/ledger-recon)** — Go. Concilia arquivos de retorno bancário CNAB240 contra o stream de eventos do ledger; worker pool com backpressure e relatório de throughput medido.

#### Sistema de Encurtador de URLs

Uma separação control plane / data plane — criação e gestão de links (Java) é um deployable separado da resolução de redirecionamento (Go), então uma indisponibilidade em um nunca derruba o outro.

- **[shortlink-api](https://github.com/dev-danilocordeiro/shortlink-api)** — Java/Spring Boot. Control plane: geração de IDs Snowflake, transactional outbox, rate limiting com Redis.
- **[shortlink-edge](https://github.com/dev-danilocordeiro/shortlink-edge)** — Go. Data plane: resolução de redirecionamento de alto volume e analytics de clique em tempo real.

#### Explorando atualmente

Fluxos de engenharia com apoio de IA — ferramentas MCP e agentes de code review, para que o tempo de engenharia vá para onde o julgamento realmente importa.

**Contato:** [email](mailto:danilocordeiro.ti@gmail.com) · [LinkedIn](https://www.linkedin.com/in/danilocordeirodev) · [portfólio](https://dev-danilocordeiro.github.io)

</details>
