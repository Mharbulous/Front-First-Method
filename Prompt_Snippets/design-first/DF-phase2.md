graph TD
    C1["2.1 AI-Assisted: Analyze Prototype to Define Data Models/Schemas"]
    
    subgraph Phase2 ["Phase 2: Deriving Backend Specifications from Validated Front-End"]
        C1 --> C1_Val{"Human Validate Data Model?"}
        C1_Val -->|Needs Revision| C1
        C1_Val -->|Approved| C2["2.2 AI-Assisted: Generate API Endpoint Specs"]
        C2 --> C2_Val{"Human Validate API Specs?"}
        C2_Val -->|Needs Revision| C2
        C2_Val -->|Approved| C3["2.3 AI-Assisted: Generate Initial Backend Structure/Stubs"]
        C3 --> C3_Val{"Human Validate Backend Structure/Stubs?"}
        C3_Val -->|Needs Revision| C3
        C3_Val -->|Approved| D_Spec["Backend Specs Finalized"]
    end
