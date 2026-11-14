# 🦀 Rusted

<p align="center">
  <img src="https://img.shields.io/badge/BUILT_WITH-RUST-FF6B35?style=for-the-badge&logo=rust&logoColor=white" />
  <img src="https://img.shields.io/badge/PROJECT-IN%20DEVELOPMENT-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DATABASE-IN--MEMORY-FF6B35?style=for-the-badge" />
</p>

<h3 align="center">
  From a simple key-value store to a distributed database.
</h3>

<p align="center">
  <i>Built from scratch. Powered by Rust. Driven by curiosity.</i>
</p>

---

## 🦀 What is Rusted?

**Rusted** is a Redis-inspired, in-memory data store being built from scratch using **Rust**.

The idea is simple: understand how databases work internally by actually building one.

Starting with a basic TCP server and a key-value storage engine, Rusted will gradually evolve into a feature-rich data store with persistence, memory management, concurrency, replication, and eventually distributed clustering.

This isn't about building everything at once.

It's about understanding every layer, getting the fundamentals right, and building upwards.

## 🔥 The Vision

```text
        A simple TCP server
                |
                v
        Key-Value Storage
                |
                v
       Data Structures
                |
                v
      Memory Management
                |
                v
          Persistence
                |
                v
       Concurrency & Pub/Sub
                |
                v
          Replication
                |
                v
       Sharding & Clustering
                |
                v
       Distributed Database
```

**Start small. Understand deeply. Scale relentlessly.**

## ⚙️ Planned Features

### Phase 01 — The Foundation
- [ ] TCP server and client connections
- [ ] RESP protocol implementation
- [ ] `SET`, `GET`, `DEL`, `PING`
- [ ] In-memory HashMap-based storage
- [ ] Basic command parser and dispatcher

### Phase 02 — The Storage Engine
- [ ] Strings, Lists, Sets and Hashes
- [ ] Sorted Sets
- [ ] TTL and key expiration
- [ ] LRU / LFU eviction policies
- [ ] Memory usage tracking

### Phase 03 — Persistence
- [ ] Append-Only File (AOF)
- [ ] RDB-style snapshots
- [ ] Database recovery after restart
- [ ] Crash recovery and data integrity

### Phase 04 — Concurrency & Communication
- [ ] Async networking with Tokio
- [ ] Concurrent client handling
- [ ] Transactions
- [ ] Pub/Sub messaging
- [ ] Performance optimizations

### Phase 05 — Distributed Systems
- [ ] Primary-replica replication
- [ ] Data sharding
- [ ] Hash-slot-based routing
- [ ] Cluster management
- [ ] Failure detection and automatic failover

### Phase 06 — Production Engineering
- [ ] Authentication and security
- [ ] Structured logging and metrics
- [ ] Fault injection and recovery testing
- [ ] Benchmarking and profiling
- [ ] Docker support
- [ ] CI/CD and documentation

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Rust** | Core implementation |
| **Tokio** | Asynchronous networking |
| **Bytes** | Efficient byte handling |
| **Serde** | Serialization |
| **Tracing** | Logging and observability |
| **Criterion** | Benchmarking |
| **Proptest** | Property-based testing |
| **Docker** | Deployment and testing |

## 🧠 Engineering Principles

- **Correctness before performance:** Make it work correctly before making it fast.
- **Understand before implementing:** Every major component should have a reason to exist.
- **Test everything:** Unit tests, integration tests, stress tests and failure scenarios.
- **Measure, don't assume:** Use benchmarks and profiling to guide optimizations.
- **Build incrementally:** Every phase should leave behind a working system.

## 📈 The Journey

Rusted will be developed incrementally, with each stage introducing new systems concepts and engineering challenges.

The long-term goal is to understand and implement the internals of a real-world database system: from networking and memory allocation to persistence, concurrency and distributed coordination.

## 🦀 Why Rust?

Rust offers memory safety without garbage collection, fine-grained control over performance, and powerful concurrency guarantees.

It's an opportunity to explore systems programming while building something substantial.

---

<p align="center">
  <img src="https://img.shields.io/badge/MADE_WITH-🦀_RUST-FF6B35?style=for-the-badge" />
</p>

<h3 align="center">Rusted — From Zero to Distributed.</h3>

<p align="center">
  <i>One command at a time. One system at a time.</i>
</p>
