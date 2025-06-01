```mermaid
graph TD
Phase1["Phase 1: Planning"] --> Phase2["Phase 2: Wireframe - Structure & Layout"]
    Phase2 --> Phase3["Phase 3: Mockup - Visual Design"]
    Phase3 --> Phase4["Phase 4: Prototype - Interactive Testing"]
    Phase4 --> Phase5["Phase 5: Deriving Backend Specifications from Validated Front-End"]
    Phase5 --> Phase6["Phase 6: AI-Assisted Backend Development & Integration"]
    Phase6 --> Phase7["Phase 7: Continuous Iteration, Testing & Refinement"]
    Phase7 --> 8["Application Complete"]
    
    Phase8 -->|Implementation Issues| Phase6
    Phase8 -->|Backend Specification Issues| Phase5
    Phase8 -->|Visual/UX Issues| Phase6
    Phase8 -->|Fundamental Structure Issues| Phase3
Phase5 -->|Requirements Issues| Phase2
    
    Version["v1.4 (June 1, 2025)"]
    
    classDef version fill:#f9f9f9,stroke:#ccc,font-size:10px
    class Version version
```
