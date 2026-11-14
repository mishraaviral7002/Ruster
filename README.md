<!--
    RUSTED — README
    Theme: Dark Terminal / Rust Orange
    Accent: #FF6B35
-->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:171717,50:9E3D1C,100:FF6B35&text=RUSTED&fontColor=FFFFFF&fontSize=85&fontAlignY=38&desc=A%20Redis-inspired%20in-memory%20database%20built%20with%20Rust&descAlignY=60&descSize=16&animation=fadeIn" width="100%" />

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=2800&pause=900&color=FF6B35&center=true&vCenter=true&width=650&lines=Built+from+scratch.+Powered+by+Rust.;From+Key-Value+Storage+to+Distributed+Systems.;One+command+at+a+time.;Understanding+the+internals+of+databases." />

<br/><br/>

[![Rust](https://img.shields.io/badge/Rust-FF6B35?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Status](https://img.shields.io/badge/STATUS-IN%20DEVELOPMENT-FF6B35?style=for-the-badge)](#)
[![Database](https://img.shields.io/badge/TYPE-IN--MEMORY%20DATABASE-222222?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/LICENSE-TBD-222222?style=for-the-badge)](#)

<br/>

**Not just another Redis clone. A journey into database internals.**

<br/>

[ Vision ](#-the-vision) •
[ Architecture ](#-architecture) •
[ Roadmap ](#-the-roadmap) •
[ Tech Stack ](#-technology-stack)

<br/>

</div>

---

## 🦀 The Project

**Rusted** is a Redis-inspired in-memory data store being developed from scratch using **Rust**.

The goal is to understand how modern databases actually work under the hood — from TCP networking and protocol parsing to memory management, persistence, concurrency, and distributed systems.

The idea isn't to build everything immediately.

It starts with something simple:

```rust
SET language "Rust"
GET language

// "Rust"
```

And gradually evolves into something much bigger.

> Start with a key. End with a cluster.

---

## 🔥 The Vision

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=17&duration=2500&pause=700&color=FF6B35&center=true&vCenter=true&width=600&lines=TCP+Server+%E2%86%92+Storage+Engine;Storage+Engine+%E2%86%92+Persistence;Persistence+%E2%86%92+Replication;Replication+%E2%86%92+Distributed+Database" />

</div>

```text
                     🦀 RUSTED
                         |
                  ┌──────┴──────┐
                  |             |
              NETWORK        STORAGE
                  |             |
              TCP Server    Key-Value Engine
                  |             |
              RESP Parser   Data Structures
                  |             |
              Commands      Memory Management
                  |             |
                  └──────┬──────┘
                         |
                    PERSISTENCE
                         |
                  AOF + Snapshots
                         |
                    CONCURRENCY
                         |
                  Async + Pub/Sub
                         |
                    REPLICATION
                         |
                  Primary / Replica
                         |
                    DISTRIBUTION
                         |
                  Sharding + Clustering
                         |
                    🚀 RUSTED
```

## ⚡ Core Features — The Roadmap

The project will be developed in stages. Every phase should result in a working, testable system.

### `01` — The Foundation

<sub>NETWORKING · PROTOCOL · COMMAND EXECUTION</sub>

- [ ] TCP server and client connections
- [ ] RESP protocol implementation
- [ ] Command parser and dispatcher
- [ ] `PING`, `SET`, `GET`, `DEL`
- [ ] HashMap-based in-memory storage
- [ ] Basic error handling

### `02` — The Storage Engine

<sub>DATA STRUCTURES · MEMORY · EXPIRATION</sub>

- [ ] Strings
- [ ] Lists
- [ ] Sets
- [ ] Hashes
- [ ] Sorted Sets
- [ ] TTL and key expiration
- [ ] LRU / LFU eviction
- [ ] Memory tracking

### `03` — Persistence

<sub>DURABILITY · RECOVERY · DATA INTEGRITY</sub>

- [ ] Append-Only File (AOF)
- [ ] RDB-style snapshots
- [ ] Database recovery after restart
- [ ] Crash recovery
- [ ] Partial-write handling

### `04` — Concurrency & Communication

<sub>ASYNC · PARALLELISM · MESSAGING</sub>

- [ ] Async networking with Tokio
- [ ] Concurrent client handling
- [ ] Transactions
- [ ] Pub/Sub messaging
- [ ] Pipelining
- [ ] Performance optimization

### `05` — Distributed Systems

<sub>REPLICATION · SHARDING · FAULT TOLERANCE</sub>

- [ ] Primary-replica replication
- [ ] Data sharding
- [ ] Hash-slot routing
- [ ] Cluster management
- [ ] Failure detection
- [ ] Automatic failover

### `06` — Production Engineering

<sub>OBSERVABILITY · TESTING · DEPLOYMENT</sub>

- [ ] Authentication and security
- [ ] Structured logging
- [ ] Metrics and monitoring
- [ ] Fault injection
- [ ] Benchmarking and profiling
- [ ] Docker deployment
- [ ] CI/CD pipeline
- [ ] Complete documentation

---

## 🏗️ Architecture

The architecture will evolve as the database grows.

| Component | Responsibility |
|---|---|
| Network Layer | TCP connections and client handling |
| Protocol Layer | RESP parsing and encoding |
| Command Engine | Command validation and execution |
| Storage Engine | In-memory data structures |
| Memory Manager | TTL, eviction and memory tracking |
| Persistence Layer | AOF, snapshots and recovery |
| Replication Layer | Synchronization between nodes |
| Cluster Layer | Sharding and node coordination |

---

## 🛠️ Technology Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=rust,docker,git,github&theme=dark" />

</div>

| Technology | Purpose |
|---|---|
| Rust | Core implementation |
| Tokio | Asynchronous networking |
| Bytes | Efficient byte handling |
| Serde | Serialization |
| Thiserror | Error handling |
| Tracing | Logging and observability |
| Criterion | Performance benchmarks |
| Proptest | Property-based testing |
| Loom | Concurrency testing |
| Docker | Containerization |

---

## 🧪 Engineering Philosophy

```text
01. CORRECTNESS FIRST
    Make it work correctly before making it fast.

02. UNDERSTAND THE INTERNALS
    Don't just use abstractions. Understand what happens underneath.

03. TEST EVERYTHING
    Unit tests, integration tests, stress tests and failure scenarios.

04. MEASURE PERFORMANCE
    Benchmark before optimizing. Never guess.

05. BUILD INCREMENTALLY
    Every stage should leave behind a working system.
```

---

## 📊 Performance & Benchmarking

Performance will be measured rather than assumed.

Planned benchmarks:

- GET / SET throughput
- Concurrent client handling
- Pipelined requests
- Large-value operations
- TTL and eviction overhead
- Persistence overhead
- Replication latency

Metrics to track:

`Throughput` · `p50 latency` · `p95 latency` · `p99 latency` · `Memory Usage`

*Benchmark results will be published once the corresponding features are implemented and tested.*

---

## 🗺️ The Journey

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:FF6B35,100:171717&section=header" width="100%"/>

**FROM ZERO TO DISTRIBUTED.**

<br/>

🦀 Learn Rust

&nbsp;&nbsp;&nbsp;↓  

⚙️ Build the storage engine

&nbsp;&nbsp;&nbsp;↓

💾 Implement persistence

&nbsp;&nbsp;&nbsp;↓

⚡ Introduce concurrency

&nbsp;&nbsp;&nbsp;↓

🌐 Build a distributed system

&nbsp;&nbsp;&nbsp;↓

🚀 **RUSTED**

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:171717,100:FF6B35&section=footer" width="100%"/>

</div>

---

## 🦀 Why Rust?

Rust provides memory safety without a garbage collector, precise control over system resources, and strong concurrency guarantees.

Building Rusted is an opportunity to explore:

- Memory ownership and allocation
- Networking and operating-system fundamentals
- Database storage engines
- Concurrency and synchronization
- Distributed systems and fault tolerance

The objective is not simply to write code that works.

**It's to understand why it works.**

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=160&color=0:FF6B35,50:9E3D1C,100:171717&section=footer&text=RUSTED&fontColor=FFFFFF&fontSize=40&fontAlignY=65&animation=fadeIn" width="100%"/>

### 🦀 Rusted — From Zero to Distributed.

<sub>One command at a time. One system at a time.</sub>

<br/>

**Built with curiosity. Engineered with Rust.**

</div>
