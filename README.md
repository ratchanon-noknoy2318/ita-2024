# Kosamphi ITA 2024: Transparency via Legacy Modernization

**Legacy PHP Architecture | Government Compliance (ITA) | Secure Document Orchestration**

Developed during my tenure at the **Office of the District Public Health, Kosamphinakhorn**, this system was engineered to digitize and automate the Integrity and Transparency Assessment (ITA) workflow. It serves as a centralized hub for public disclosure and administrative accountability.

---

## 1. System Architecture & Legacy Stack

The project was built using a **Reliable Legacy Stack** to ensure 100% compatibility with existing hospital-grade hosting environments while maintaining high security and performance standards.



```mermaid
graph TD
    %% User Layer
    User[Public / Admin] -->|HTTP Request| Web[Web Interface: HTML5/CSS3]

    %% Logic Layer
    Web -->|Processing| App[Legacy PHP Engine]
    
    %% Middleware/Logic
    App -->|Auth| Sec[Session-based Authentication]
    App -->|CRUD Operations| DB[(MySQL Database)]

    %% Deployment
    subgraph Infrastructure [MOPH Production Environment]
        App
        DB
    end

    %% Styling
    style App fill:#777bb4,color:#fff
    style DB fill:#4479a1,color:#fff
    style Infrastructure fill:#f5f5f5,stroke:#333,stroke-dasharray: 5 5
