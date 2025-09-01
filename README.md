# Deciding on a Fit-for-Purpose Programming Language  
**Opinionated Programming Language Decision Guide**  

---

## Prerequisites  
- **Architecture**: Microservice-based (service mesh) with polyglot support.  
- **Application Types**:  
  - Progressive Web Applications (PWA)  
  - Single Page Applications (SPA)  
  - Backend-for-Frontend (BFF)  
- **Related Resources**:  
  - [Security Architecture](https://github.com/pettersson-dev/security-architecture)  
  - [API Integration Architecture](https://github.com/Pettersson-dev/Integration-architecture/blob/main/api-integration.md)  
  - [Application Architecture](https://github.com/pettersson-dev/application-architecture)  

---

## Shortlist of Languages  

- **General Purpose**: C#, C++, Go, Java, Kotlin, Python, Rust, Scala  
- **Functional/Concurrent**: Clojure, Elixir, Erlang  
- **Scripting & Prototyping**: JavaScript, Node.js, Groovy, PHP, Ruby  
- **Frontend**: TypeScript, Dart, Swift, Objective-C  
- **Specialized**: Rust, Scala (for highly concurrent, secure or data-heavy systems)  

---

## Decision Tree  

### Backend Languages  

#### Go  
- **Default choice** for small, efficient, and secure microservices.  
- **Good Fit**:  
  - IoT, edge, or strict hardware requirements.  
  - High-security, low-dependency services.  
  - Stateless APIs or CLI tools.  
- **Bad Fit**:  
  - Very large/complex systems.  
  - Heavy library or dependency needs.  

---

#### Java / Kotlin / Scala  
- **Enterprise backbone** for integrations, messaging, and concurrent systems.  
- **Good Fit**:  
  - Mature ecosystem with rich libraries.  
  - Medium–large systems (finance, telecom, BI, AI pipelines).  
  - JVM optimizations for performance and concurrency.  
- **Bad Fit**:  
  - Tight hardware constraints.  
  - High-performance native apps (gaming, real-time image processing).  

---

#### JavaScript / Node.js  
- **Bridge between frontend and backend**, ideal for rapid development.  
- **Good Fit**:  
  - Real-time apps (chat, notifications, streaming).  
  - Prototyping and POCs.  
  - Unified full-stack JavaScript development.  
- **Bad Fit**:  
  - CPU-heavy or multi-threaded apps.  
  - Monolithic enterprise systems.  

---

#### C# (.NET Core)  
- Best for orgs already invested in the **Microsoft ecosystem**.  
- **Good Fit**:  
  - Medium–large enterprise solutions.  
  - MVC architectures, Azure-native services.  
  - Strong Windows ecosystem integrations.  
- **Bad Fit**:  
  - Lightweight services needing minimal boilerplate.  
  - Teams with no Microsoft background.  

---

#### Python  
- **Versatile scripting/data language** with global adoption.  
- **Good Fit**:  
  - Data science, AI/ML, BI.  
  - Rapid prototyping, automation, scripting.  
  - IO-heavy systems, APIs, orchestration.  
- **Bad Fit**:  
  - Security-critical or high-performance applications.  
  - Mobile, embedded, or game dev.  
  - Large-scale monoliths.  

---

#### Rust  
- **Safe systems language** combining C++ performance with memory safety.  
- **Good Fit**:  
  - High-security or performance-critical services.  
  - Cloud-native infrastructure (e.g., WASM, Kubernetes tooling).  
  - Cryptography, embedded, IoT.  
- **Bad Fit**:  
  - Rapid prototyping (steeper learning curve).  
  - Teams lacking low-level expertise.  

---

#### Elixir / Erlang  
- **Functional, concurrent** platforms (built on BEAM VM).  
- **Good Fit**:  
  - Telecom-grade concurrent systems.  
  - Chat, messaging, streaming, distributed systems.  
  - Fault-tolerant microservices.  
- **Bad Fit**:  
  - Teams without functional programming skills.  
  - Traditional enterprise integrations.  

---

### Frontend & Client  

#### Browser Apps  
- **JavaScript**: Default language, universal browser support.  
- **TypeScript**: Strongly-typed superset of JS, preferred for long-term maintainability.  

#### Mobile Apps  
- **Native iOS** → **Swift** (modern, safe, Apple ecosystem).  
- **Native Android** → **Kotlin** (first-class Android support).  

**Choose Native if:**  
- Differentiation through platform features is required.  
- Direct access to device hardware/APIs is critical.  

---

## Cross-Cutting Considerations  

- **Polyglot**: Service mesh must handle language diversity seamlessly.  
- **Ecosystem Fit**: Choose languages aligned with organizational expertise and toolchains.  
- **Future-Proofing**: Prefer languages with strong community, long-term vendor support, and active development.  
- **DevOps/CI/CD**: Consider tooling maturity (linting, testing, containerization).  
- **Security**: Some languages have stronger ecosystems for secure coding (e.g., Rust, Go, TypeScript).  

---

## Summary  
- **Go** → Small, secure, efficient services.  
- **Java/Kotlin/Scala** → Enterprise-scale, concurrent, integration-heavy.  
- **Node.js** → Real-time and full-stack synergy.  
- **C#** → Microsoft/Azure-heavy environments.  
- **Python** → Data, AI/ML, prototyping.  
- **Rust** → Performance + security critical workloads.  
- **Elixir/Erlang** → Highly concurrent distributed systems.  
- **TypeScript** → Best frontend and long-term maintainability.  
- **Swift/Kotlin** → Native mobile excellence.  