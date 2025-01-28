# Work in Progress  

# Deciding on a Fit-for-Purpose Programming Language  
**Opinionated Programming Language Decision Tree**  

---

## **Prerequisites**  
- **Architecture**: Microservice architecture (service mesh) supporting polyglot languages.  
- **Application Type**: Progressive Web Applications (PWA), Single Page Applications (SPA), and backend-for-frontend (BFF).  
- **Related Resources**:  
   - [Security Architecture](https://github.com/pettersson-dev/security-architecture)  
   - [API Integration Architecture](https://github.com/Pettersson-dev/Integration-architecture/blob/main/api-integration.md)  
   - [Application Architecture](https://github.com/Pettersson-dev/application-architecture)  

---

## **Shortlist of Programming Languages**  
The following languages have been shortlisted for evaluation based on specific use cases:  

- **General Purpose**: C#, C++, Go, Java, Kotlin, Python, Rust, Scala  
- **Functional**: Clojure, Elixir, Erlang  
- **Scripting and Prototyping**: JavaScript, Node.js, Groovy, PHP, Ruby  
- **Frontend**: TypeScript, Dart, Swift, Objective-C  
- **Specialized**: Rust, Scala (for highly concurrent or secure systems)  

---

## **Decision Tree**  

### **Backend**  

#### **Go**  
- **Default choice** for simple, efficient, and stable services with minimal dependencies.  
- **Good Fit**:  
  - Strict hardware requirements (e.g., IoT).  
  - High security requirements.  
  - Small, standalone services.  
- **Bad Fit**:  
  - Large, complex implementations.  
  - Dependency management and extensive library requirements.  

---

#### **Java/Kotlin/Scala**  
- **General purpose** solutions, particularly suited for integrations, messaging, and highly concurrent systems.  
- **Good Fit**:  
  - Extensive libraries and mature ecosystems.  
  - Medium to large-scale implementations.  
  - Use cases in security, mathematics, or business intelligence (BI).  
- **Bad Fit**:  
  - Strict hardware constraints.  
  - Heavy IO operations.  
  - Resource-heavy applications (e.g., image processing).  

---

#### **JavaScript/Node.js**  
- Ideal for **real-time applications** and systems requiring seamless integration between frontend and backend.  
- **Good Fit**:  
  - Prototyping.  
  - Single-threaded tasks.  
  - Optimized for IO and transformation support.  
  - Unified language across the stack.  
- **Bad Fit**:  
  - CPU-intensive or multi-threaded applications.  
  - Large, monolithic systems.  

---

#### **C# (.NET Core)**  
- A powerful choice for organizations already invested in Microsoft’s ecosystem.  
- **Good Fit**:  
  - Small to large-scale implementations.  
  - MVC architecture for frontend.  
  - Integration with Microsoft-based tools (e.g., Azure, Service Fabric).  
- **Bad Fit**:  
  - Limited libraries (though improving).  
  - Small systems needing minimal boilerplate.  

---

#### **Python**  
- **Versatile language** best suited for scripting, data analysis, and prototyping.  
- **Good Fit**:  
  - Data-heavy applications (Math, BI, AI).  
  - Scripting and prototyping.  
  - Applications optimized for IO.  
- **Bad Fit**:  
  - High-security applications.  
  - Mobile or game development.  
  - Large, monolithic applications.  

---

### **Frontend/Client**  

#### **Browser-Based Applications**  
- **JavaScript**: The default language for client-side applications.  
- **TypeScript**: A superset of JavaScript offering better type safety and tooling.  

#### **Mobile Applications**  
- **Native Development**:  
  - **Swift**: Best suited for iOS development.  
  - **Kotlin**: Ideal for Android development.  
- **When to Choose Native**:  
  - To differentiate through platform-specific features.  
  - To leverage the latest advancements offered by the platform.  

---

## **Additional Notes**  
- **Polyglot Considerations**: Ensure the service mesh supports interoperability and integration between chosen languages.  
- **Ecosystem Alignment**: Opt for languages that align with organizational expertise and existing tools.  
- **Future-proofing**: Evaluate community support and updates for long-term sustainability 