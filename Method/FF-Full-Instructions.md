# Front-End First AI Development Instructions

## A. Preamble: Guiding Principles for the AI Agent



---

## B. Phase 1: Front-End Definition, Design, and (AI-Assisted) Prototyping

### Step 1.1: Elicit and Clarify UI/UX Requirements & User Flows

- Engage with the human user to gather detailed requirements for the application's UI/UX. Ask clarifying questions to understand:
  - Target users
  - Key user goals
  - Primary tasks
  - Essential features
  - Desired user journeys

- Collaboratively define and document primary user flows (e.g., user registration, item purchase, data visualization). You can assist by suggesting common patterns or asking targeted questions to ensure completeness.

- Based on this, list all distinct views/screens required for the application.

### Step 1.2: Generate Front-End Mockups/Wireframes (AI-assisted, based on requirements)

- For each identified view/screen, and based on the user flows, assist in generating initial wireframes or low-fidelity mockups. You can propose layouts and common UI components (buttons, forms, tables, navigation menus) suitable for the described functionality.

- Present these visual suggestions for human review and iterate based on feedback until the structure of each screen is approved.

### Step 1.3: Develop Interactive Front-End Prototypes (Static HTML/CSS/JS or using UI library components with mock data)

- Translate the approved wireframes/mockups into interactive front-end prototypes. This can be static HTML, CSS, and JavaScript, or utilize components from a specified UI library/framework.

- Focus on accurately representing the UI elements, layout, navigation, and basic interactivity (e.g., button clicks leading to other views, form field interactions). Use placeholder/mock data to simulate dynamic content, reflecting practices where developers use previously prepared static data for initial UI work.

- Ensure the prototype is responsive and adheres to any specified design guidelines.

### Step 1.4: Stakeholder/User Validation Loop for Front-End Prototype

- Present the complete interactive front-end prototype for thorough review by the human user/stakeholders.

- Prompt for specific feedback on:
  - Usability
  - Completeness of features
  - Correctness of user flows
  - Overall design

- Document all requested changes. Iterate on Step 1.3 and this step until the front-end prototype is fully approved and considered stable. **This validated prototype is now the primary specification.**

---

## C. Phase 2: Deriving Backend Specifications from Validated Front-End

### Step 2.1: Analyze Validated Front-End for Data Entities, Attributes, and Relationships

- Systematically examine every element and interaction in the approved front-end prototype.

- Identify all distinct data entities implied by the UI (e.g., 'User', 'Product', 'Order', 'Comment').

- For each entity, list its attributes (e.g., for 'User': username, email, password_hash, creation_date) based on form fields, displayed data, etc.

- Determine relationships between entities (e.g., a 'User' can have many 'Orders'; an 'Order' contains many 'Products'). Specify cardinality (one-to-one, one-to-many, many-to-many).

- Present this proposed data model (entities, attributes, relationships) for human validation.

### Step 2.2: Define API Endpoints, Request/Response Payloads based on UI interactions

- For each user interaction in the front-end that requires data from or sends data to a server (e.g., form submissions, data loading for a table, button clicks triggering actions), define a corresponding API endpoint.

- Specify:
  - HTTP method (GET, POST, PUT, DELETE)
  - URL path
  - Expected request payload (data structure and types)
  - Expected response payload (data structure and types)
  
  This aligns with AI's capability to assist in generating API requests and hooks.

- Ensure API design is RESTful or follows specified architectural patterns.

- Present the complete list of API endpoints and their specifications for human validation.

### Step 2.3: Outline Backend Modules, Services, and Core Logic Stubs

- Based on the data model and API endpoints, propose a modular structure for the backend (e.g., user_service, product_service, order_service).

- For each module/service, list the core functions/methods required to handle the defined API endpoints and business logic (e.g., createUser(userData), getProductById(productId), placeOrder(orderDetails)).

- Write initial stubs or pseudo-code for this core logic, clearly indicating dependencies on data models and other services.

- Present this backend structural outline and logic stubs for human validation.

---

## D. Phase 3: AI-Assisted Backend Development and Integration (Iterative per Feature/Module)

### Step 3.1: Generate Backend Boilerplate Code (e.g., controllers, models, basic CRUD)

- For an approved module/feature: Generate the boilerplate code for data models/schemas based on Step 2.1.

- Generate controller/router files with empty methods for the API endpoints defined in Step 2.2.

- Implement basic CRUD (Create, Read, Update, Delete) operations for entities where applicable, ensuring data validation based on front-end implied constraints.

- Present generated code for review.

### Step 3.2: Implement Core Business Logic for each feature, guided by front-end context

- Flesh out the core business logic within the stubs defined in Step 2.3, ensuring it correctly processes inputs from the front-end (via APIs) and produces the expected outputs/state changes.

- Pay close attention to any specific business rules or constraints discussed during requirements gathering or implied by the front-end design. AI has shown effectiveness in handling data processing and merging logic.

- Generate this code iteratively, perhaps function by function, for human review and validation.

### Step 3.3: Iteratively Connect Front-End Components to Live Backend Endpoints

- Once a backend API endpoint is implemented and validated, guide the human developer (or assist if capable) in updating the front-end prototype to replace mock data/static interactions with live calls to this endpoint.

- Test this specific integration thoroughly. This is an iterative process: implement a backend piece, connect front-end, test, repeat.

---

## E. Phase 4: Continuous Iteration, Testing, and Refinement

### Step 4.1: Implement Comprehensive Testing (Unit, Integration, End-to-End for UI-Backend flow)

- For all AI-generated backend code, assist in generating unit tests that cover individual functions and logic.

- Define and help set up integration tests to verify interactions between different backend modules/services.

- Outline end-to-end test scenarios that trace complete user flows from the (now connected) front-end through the backend and back to the UI. AI can be instrumental in devising test scripts.

### Step 4.2: Refine based on test results and further feedback

- Analyze test results. If failures occur, assist in debugging by identifying potential error sources in the AI-generated code, leveraging AI's strengths in error analysis and explanation.

- Incorporate any further user/stakeholder feedback that arises from testing the integrated application.

- Repeat development and testing steps as needed until the feature/application meets all requirements.

---

## F. General Directives for the AI Agent

### Core Operational Guidelines:

1. **Decomposition as Default:** Always attempt to break down complex requests into a series of smaller, verifiable steps. If a request seems too large, ask for it to be broken down further.

2. **Proactive Validation Prompts:** Do not wait to be asked for validation. At the conclusion of any significant step (e.g., generating a data model, defining a set of API endpoints, coding a service module), explicitly state what you have done and ask for human review and approval before proceeding.

3. **Code Quality and Security:** When generating code, adhere to best practices for readability, maintainability, performance, and security relevant to the specified technology stack. If security implications are identified (e.g., handling user passwords, input sanitization), highlight them and suggest appropriate measures, referencing established security best practices such as sanitizing user input and following OAuth standards.

4. **Ambiguity Resolution:** If requirements derived from the front-end or subsequent instructions are unclear, ambiguous, or contradictory, immediately halt and request clarification from the human user. Do not make assumptions on critical aspects.

5. **Contextual Awareness:** Continuously refer back to the validated front-end prototype and previously approved specifications to maintain context and ensure consistency in your outputs.

6. **Technology Stack Adherence:** Ensure all generated code, architectural suggestions, and tool recommendations are compatible with the project's defined technology stack.

---

## Summary Workflow

```
Phase 2: Front-End First
├── Requirements Gathering
├── Wireframes/Mockups
├── Interactive Prototypes
└── Stakeholder Validation ✓

Phase 5: Backend Specification
├── Data Model Analysis
├── API Endpoint Definition
└── Backend Architecture ✓

Phase 6: Implementation
├── Boilerplate Generation
├── Business Logic Implementation
└── Frontend-Backend Integration ✓

Phase 7: Testing & Refinement
├── Comprehensive Testing
└── Iterative Improvements ✓
```

> **Key Principle:** Each phase requires explicit human validation before proceeding to the next phase. The AI agent should always ask for approval and confirmation before moving forward.