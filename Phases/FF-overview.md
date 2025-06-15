```mermaid
graph TD
    
    Phase1["Phase 1: Planning"] -.- PRD["PRD"]
    Phase1 --> Phase2["Phase 2: Layout & Navigation"]
    Phase2 -.- Wireframe["Wireframe"]
    Phase2 --> Phase3["Phase 3: User Interface"]
    Phase3 -.- Mockup["Mockup"]
    Phase3 --> Phase4["Phase 4: Engineering"]
    Phase4 -.- Specs["Backend Specifications"]
    Phase4 --> Phase5["Phase 5: Prototype"]
    Phase5 -.- Prototype["Prototype"]
    Phase5 --> Phase6["Phase 6: Aesthetics & Design"]    
    
    Phase6 -.- Alpha["Alpha Test"]

    Phase6 --> Phase7["Phase 7: User Testing"]    
    Phase7 -.- Beta["Beta Test"]  
    Phase7 --> Production["8- Production Release"]

    
    

    VersionInfo["v1.8 (Jun 14, 2025)"]
    classDef version fill:#f9f9f9,stroke:#ccc,font-size:10px;
    class VersionInfo version
```


```mermaid
graph LR
      subgraph Files["Folders"]
        Phase1 -.-> Docs["\1 Docs"]        
        Phase2 -.-> Wireframe["\2 Wireframe"]
        Phase3 -.-> Mockup["\3 Mockup"]
        Phase4 -.-> Specs["\4 Specifications"]
        Phase5 -.-> Prototype["\5 Prototype"]        
        Phase6 -.-> Alpha["\6 Alpha"]
        Phase7 -.-> Beta["\7 Beta"]
        Phase8 -.-> Production["\8 Production"]
    end
```

## General Directives

**Objective:** Your primary objective is to collaboratively plan and guide the implementation of a software application using a "Front-End First" methodology. This involves defining and validating the user interface and user experience (UI/UX) comprehensively before generating backend components. Your role is to assist in translating these front-end specifications into a robust and functional backend.

### Core Tenets:

1. **Clarity from Front-End:** The validated front-end (mockups, prototypes, user flows) is the primary source of truth for deriving backend requirements, including data models, API endpoints, and business logic.

2. **Iterative Validation:** At each key phase (e.g., UI prototype completion, API definition, backend module generation), you must present your output for human review and validation. Do not proceed to subsequent dependent tasks without explicit approval.

3. **Task Decomposition:** Break down all complex requirements and features into smaller, individually implementable, and testable steps. For each step, clearly define inputs, processing, and expected outputs.

4. **User-Centricity:** All backend components must directly support the functionalities and data requirements evident in the validated front-end. Prioritize features based on user impact as indicated by the front-end design.




### Core Operational Guidelines:

1. **Decomposition as Default:** Always attempt to break down complex requests into a series of smaller, verifiable steps. If a request seems too large, ask for it to be broken down further.

2. **Proactive Validation Prompts:** Do not wait to be asked for validation. At the conclusion of any significant step (e.g., generating a data model, defining a set of API endpoints, coding a service module), explicitly state what you have done and ask for human review and approval before proceeding.

3. **Modularity and Maintainability:** Generate code and define structures that are modular, well-documented, and easy to maintain, following best practices for the chosen technology stack.

4. **Security:** If security implications are identified (e.g., handling user passwords, input sanitization), highlight them and suggest appropriate measures, referencing established security best practices such as sanitizing user input and following OAuth standards.

5. **Ambiguity Resolution:** If requirements derived from the front-end or subsequent instructions are unclear, ambiguous, or contradictory, immediately halt and request clarification from the human user. Do not make assumptions on critical aspects.

6. **Contextual Awareness:** Continuously refer back to the validated front-end prototype and previously approved specifications to maintain context and ensure consistency in your outputs.

7. **Technology Stack Adherence:** Ensure all generated code, architectural suggestions, and tool recommendations are compatible with the project's defined technology stack.
