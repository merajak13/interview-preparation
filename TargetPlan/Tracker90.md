# System Design Interview Cracker Track

## 🎯 Goal

Prepare for Java Backend / Microservices system design interviews with a practical, interview-focused approach covering:

- HLD / High-Level System Design
- LLD / Low-Level Design
- Distributed Systems
- Scalability and Performance
- Database Design
- Caching
- Kafka / Event-Driven Architecture
- API Design
- Reliability and Fault Tolerance
- GenAI System Design
- Real Interview Problems

---

# PHASE 0 — Foundation

**Duration: 3–4 days**

## 0.1 Scalability Fundamentals

- [ ] Vertical vs Horizontal Scaling
- [ ] Stateless vs Stateful Services
- [ ] Load Balancing
- [ ] Reverse Proxy
- [ ] Service Discovery
- [ ] API Gateway

## 0.2 Availability & Reliability

- [ ] Availability
- [ ] Reliability
- [ ] Fault Tolerance
- [ ] Single Point of Failure
- [ ] Failover
- [ ] Redundancy
- [ ] Graceful Degradation

## 0.3 Performance

- [ ] Latency
- [ ] Throughput
- [ ] QPS / RPS
- [ ] Concurrent Users
- [ ] Bottleneck Identification
- [ ] Capacity Estimation

## 0.4 CAP Theorem

- [ ] Consistency
- [ ] Availability
- [ ] Partition Tolerance
- [ ] CP vs AP
- [ ] Network Partition
- [ ] Real-world CAP examples

---

# PHASE 1 — System Design Building Blocks

**Duration: 7 days**

## 1. Load Balancer

- [ ] Why Load Balancer?
- [ ] L4 vs L7
- [ ] Round Robin
- [ ] Least Connections
- [ ] Health Checks
- [ ] Sticky Sessions
- [ ] Load Balancer Failure

**Interview Question:**

> How would you distribute 1 million requests across 10 servers?

## 2. Database

### SQL

- [ ] Indexing
- [ ] Composite Indexes
- [ ] Query Optimization
- [ ] Transactions
- [ ] ACID
- [ ] Isolation Levels
- [ ] Normalization
- [ ] Denormalization
- [ ] Replication
- [ ] Read Replicas

### NoSQL

- [ ] Why NoSQL?
- [ ] Key-Value Databases
- [ ] Document Databases
- [ ] Wide-Column Databases
- [ ] CAP Trade-offs

**Priority for this profile:** PostgreSQL + Redis.

---

# PHASE 2 — Caching

**Duration: 2–3 days**

- [ ] Why Caching?
- [ ] Cache-Aside
- [ ] Read-Through
- [ ] Write-Through
- [ ] Write-Back
- [ ] Cache Invalidation
- [ ] TTL
- [ ] Eviction Policies
- [ ] Cache Stampede
- [ ] Cache Penetration
- [ ] Cache Consistency
- [ ] Redis Clustering

**Interview Problem:**

> Design a product catalog with Redis caching.

---

# PHASE 3 — Messaging & Kafka

**Duration: 4 days**

## Messaging Fundamentals

- [ ] Synchronous vs Asynchronous
- [ ] Queue vs Topic
- [ ] Producer
- [ ] Consumer
- [ ] Broker
- [ ] Partition
- [ ] Offset

## Kafka

- [ ] Topics
- [ ] Partitions
- [ ] Consumer Groups
- [ ] Replication
- [ ] Ordering
- [ ] Offset Management
- [ ] At-Least-Once Delivery
- [ ] At-Most-Once Delivery
- [ ] Exactly-Once Concepts
- [ ] Retry
- [ ] Dead-Letter Topic
- [ ] Idempotency

**Interview Question:**

> What happens if a Kafka consumer processes a message but crashes before committing the offset?

---

# PHASE 4 — API & Microservices Design

**Duration: 4 days**

- [ ] REST API Design
- [ ] HTTP Methods
- [ ] HTTP Status Codes
- [ ] Pagination
- [ ] Filtering
- [ ] Sorting
- [ ] API Versioning
- [ ] Idempotency
- [ ] Rate Limiting
- [ ] Authentication
- [ ] Authorization
- [ ] JWT
- [ ] OAuth2 Basics
- [ ] API Gateway
- [ ] Service Discovery
- [ ] Inter-Service Communication
- [ ] REST vs gRPC

**Interview Question:**

> Why would you choose gRPC instead of REST?

---

# PHASE 5 — Distributed Systems

**Duration: 7 days**

- [ ] Distributed Transactions
- [ ] Two-Phase Commit
- [ ] Saga Pattern
- [ ] Eventual Consistency
- [ ] Strong Consistency
- [ ] Distributed Locking
- [ ] Leader Election
- [ ] Consensus Basics
- [ ] Replication
- [ ] Sharding
- [ ] Partitioning
- [ ] Consistent Hashing
- [ ] Quorum
- [ ] Idempotency
- [ ] Retry
- [ ] Timeout
- [ ] Circuit Breaker
- [ ] Bulkhead Pattern

## Reference Architecture

```text
Request
   ↓
API Gateway
   ↓
Service
   ↓
Database
   ↓
Kafka
   ↓
Consumer
   ↓
Another Service