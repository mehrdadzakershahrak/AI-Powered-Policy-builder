# 🧭 System Design Framework (Reusable Guide)

Use this framework as a repeatable guide to design backend systems — from whiteboard interviews to real-world architecture planning.

---

## 1. 📌 Problem Understanding & Clarification
- What is the system supposed to do?
- Who are the users (external, internal, both)?
- What are the boundaries of the system?
- What assumptions or constraints should we acknowledge?

---

## 2. ✅ Functional Requirements
- What features or operations must be supported?
- Examples: login, upload, notifications, real-time collaboration
- What does each user or system role need to do?
- What APIs or endpoints are required?

---

## 3. ⚙️ Non-Functional Requirements

| Attribute       | Questions to Ask                                         |
|----------------|-----------------------------------------------------------|
| Latency        | How fast must the system respond?                         |
| Throughput     | How many requests or users per second?                    |
| Availability   | Can it tolerate downtime? Should it be globally available?|
| Scalability    | How will it grow? (vertical/horizontal/distributed)       |
| Security       | What data is sensitive? Auth & encryption needs?          |
| Maintainability| How modular, clean, and testable should it be?            |

---

## 4. 🧱 Data Modeling
- Identify entities (e.g., User, Post, Policy, Order)
- Define relationships (1:1, 1:N, N:M)
- Choose database types:
  - SQL for consistency and complex relationships
  - NoSQL for flexible, high-scale data
- Consider schema design and indexes

---

## 5. 🗺️ High-Level Architecture Design
- What are the core components/services?
- How do they interact?
- Include:
  - API Gateway / Load Balancer
  - App Services / Business Logic
  - Databases
  - File Storage / CDN
  - Caches
  - Message Queues
- Optional: add an architecture diagram (e.g., Mermaid)

---

## 6. 🚀 Scaling Strategy
- Application layer: horizontal scaling, stateless design
- Database:
  - Read replicas, partitioning/sharding, eventual consistency
- Queue-based async: offload heavy jobs to Sidekiq, Kafka, etc.
- Cache:
  - Redis/Memcached for hot data
- CDN:
  - Serve static/media content from edge nodes

---

## 7. ⚖️ Trade-offs, Bottlenecks, and Failures
- Identify likely points of failure
- Graceful degradation — what can fail without full outage?
- Trade-offs between:
  - Consistency vs availability (CAP)
  - Cost vs latency
  - Simplicity vs flexibility

---

## 8. 🔐 Security, Privacy & Observability
- Authentication: JWT, OAuth, sessions
- Authorization: RBAC/ABAC (Pundit, CanCanCan)
- Rate limiting, input validation, CSRF/XSS protection
- Observability stack:
  - Logs, metrics, alerts
  - Tools: ELK, Prometheus/Grafana, Sentry

---

## 9. 🔄 Extensibility & Maintainability
- Can new modules be added without rewriting the system?
- How easy is debugging and testing?
- Codebase should follow:
  - Clean architecture
  - Clear separation of concerns
  - Minimal coupling

---

## 10. 🧠 Communication Summary (for Interviews)

When explaining your design:
- Start with use cases and users
- Outline architecture progressively
- Justify each major design choice
- Mention trade-offs
- Be ready to zoom in (deep dive) into a few key areas

---

Use this guide across multiple projects or interviews to maintain a sharp, methodical approach to system design.
