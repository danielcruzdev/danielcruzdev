<div align="center">

# Daniel Cruz

### Software Architect · .NET · Distributed Systems

Building financial systems that stay correct when things go wrong.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-danielafcruz-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/danielafcruz/)
[![LeetCode](https://img.shields.io/badge/LeetCode-danielaffcruz-FFA116?style=for-the-badge&logo=leetcode&logoColor=white)](https://leetcode.com/u/danielaffcruz/)

</div>

---

## About

Software Architect and Developer at **Banco Sofisa**, working on backend systems in the .NET ecosystem.

My focus is the part of software that only shows up under failure: consistency across service boundaries, idempotency, compensation, and the observability you need to prove any of it works. Most of my repositories here are built around a single question — *what happens when a dependency goes down mid-transaction?*

- 🏗️ Distributed systems, event-driven architecture, and pragmatic API design
- 📐 I document decisions as ADRs with the alternatives I rejected and why
- 📊 I state non-functional requirements as numbers and test against them
- 🌍 Based in Brazil (UTC−3) · Working in English and Portuguese

---

## Featured Work

### 💰 [dotnet-cqrs-cashflow](https://github.com/danielcruzdev/dotnet-cqrs-cashflow)

Two-service cash flow platform built around one hard requirement: **the transaction service stays available even when the consolidation service is completely down** — and there is a test that proves it.

Transactional Outbox, idempotent consumers, compensating reversals, circuit breakers, and liveness/readiness separation. Ships with 9 ADRs, C4 diagrams, failure-path sequence diagrams, an operational runbook, and k6 load tests with SLO thresholds enforced in CI.

| Measured | Result | SLO |
|---|---|---|
| p95 latency | **1.98 ms** | < 100 ms |
| Error rate @ 50 req/s | **0%** | ≤ 5% |
| Read-model consistency lag | **~2.2 s** | < 5 s |

`.NET 10` `CQRS` `Outbox` `RabbitMQ` `PostgreSQL` `Redis` `Polly` `Testcontainers` `k6`

---

### 💳 [dotnet-api-fintech-ledger](https://github.com/danielcruzdev/dotnet-api-fintech-ledger)

Double-entry bookkeeping API where **balances can never drift**: entries are append-only, corrections happen through reversals rather than updates, and concurrent writes are resolved with optimistic concurrency. Integration tests run against a real PostgreSQL instance.

`.NET 10` `Minimal APIs` `PostgreSQL` `EF Core` `Vertical Slice` `Testcontainers`

---

### 🤖 [dotnet-mcp-server](https://github.com/danielcruzdev/dotnet-mcp-server)

An AI agent and **Model Context Protocol server written from scratch** — no SDK. JSON-RPC 2.0 over stdio with Content-Length framing, tool-calling orchestration, path-traversal protection on file access, and 18 scenario tests covering realistic agent workflows.

`.NET 10` `MCP` `JSON-RPC 2.0` `AI Agents` `OpenAI API` `xUnit`

---

### 🚌 [Lib.MeshBus](https://github.com/danielcruzdev/Lib.MeshBus)

Messaging abstraction that lets application code publish and subscribe without binding to a provider SDK. Factory-based multi-broker support, pluggable serialization, and a correlation-aware message envelope. Published to NuGet.

`.NET 10` `Kafka` `RabbitMQ` `Azure Service Bus` `NuGet`

---

### 🧱 [dotnet-vertical-slice-architecture](https://github.com/danielcruzdev/dotnet-vertical-slice-architecture)

Task Manager API where each use case owns its endpoint, handler, validation, and tests — organized by feature instead of by technical layer.

`.NET 10` `Vertical Slice` `CQRS` `MediatR` `Carter` `FluentValidation`

---

### ⚡ [dotnet-api-rate-limit](https://github.com/danielcruzdev/dotnet-api-rate-limit)

Working comparison of the four ASP.NET Core rate limiting strategies — Fixed Window, Sliding Window, Token Bucket, and Concurrency Limiter — with the trade-offs of each.

`.NET` `ASP.NET Core` `Minimal APIs` `Rate Limiting`

---

## Tech

**Core** — C# · .NET 10 · ASP.NET Core · Minimal APIs · EF Core · Dapper

**Architecture** — CQRS · Vertical Slice · DDD · Transactional Outbox · Saga & compensation · Idempotency

**Data & Messaging** — PostgreSQL · Redis · RabbitMQ · Kafka · Azure Service Bus

**Reliability & Ops** — OpenTelemetry · Polly · Docker · GitHub Actions · k6 · Testcontainers · xUnit

**AI** — Model Context Protocol · OpenAI API · tool-calling agents

---

## Currently

Working through the operational side of the cash flow platform — Kubernetes deployment, autoscaling driven by queue depth, and infrastructure as code.

<!--
## Writing
Add articles here as they are published — this section is intentionally empty
rather than filled with placeholders.
-->

---

## Contact

Open to conversations about distributed systems, architecture, and interesting problems.

[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/danielafcruz/)

<div align="center">
  <br>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/danielcruzdev/danielcruzdev/output/github-contribution-grid-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/danielcruzdev/danielcruzdev/output/github-contribution-grid-snake.svg">
    <img alt="contribution grid snake animation" src="https://raw.githubusercontent.com/danielcruzdev/danielcruzdev/output/github-contribution-grid-snake.svg">
  </picture>
</div>
