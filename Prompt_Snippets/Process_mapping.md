# Use diagrams to plan and describe processes and complex alogrithims.

When planning complex implementations, start by internally creating a JSON object that describes the diagrams elements (nodes, actors, states), their properties (labels, shapes), and their relationships (links, messages, transitions) along with any associated logic (conditions, loops).  For example, for a flowchart, the JSON object might define an array of nodes (each with an ID, label, and shape) and an array of edges (each with a source ID, target ID, and label). 

# When seeking user validation and approval your primary goal is to clearly communicate your proposed implementation plan by using diagrams rather than raw code snippets.

Use the following step-by-step proces to create explanatory diagrams:

1. Analyze the Implementation Plan and Identify Key Visualizable Aspects:
Based on the user's request (epic, story, feature), break down your proposed implementation plan into core components, processes, workflows, interactions, or state changes.
Determine which aspects of this plan would be most effectively communicated to the user through a visual diagram to enhance their understanding. Focus on clarity and the most critical information. 

2. Select the optimal diagram type for explanation:
Flowchart: To illustrate a sequence of steps, decision logic within the implementation, or a high-level process flow.    
Sequence Diagram: To detail interactions between different components, modules, or services in the proposed implementation, showing the order of operations.    
State Diagram: To represent the different states an entity within your proposed feature might go through and the triggers for those transitions.    
Class Diagram: If explaining the static structure of new or modified classes and their relationships is key to understanding the plan.    
Activity Diagram: For more complex workflows within the implementation, showing parallel processes, conditions, and loops.
Other types (Component, Deployment, ERD) if they are uniquely suited to explain a specific part of your plan.

3. Propose Diagramming Tools and Seek User Verification based on the chosen diagram type and the complexity of the information to be conveyed:
Mermaid: Your default choice for simpler flowcharts or sequence diagrams, especially if the user might want to embed them easily in Markdown.    
PlantUML: If the plan requires detailed UML diagrams (complex sequence, activity, state, or class diagrams) due to its expressive power.    
D2 (Declarative Diagramming Language): For software architecture diagrams where a high-quality, clear layout is paramount, leveraging its ELK layout engine.    
Graphviz (DOT Language): For abstract graph representations or highly complex dependency mappings where its layout algorithms excel.    
Communicate Your Choice to the User: Explain which tool you recommend and why (e.g., "To illustrate the interaction between these services for feature X, I plan to generate a PlantUML sequence diagram because it clearly shows the message flow over time. Would that work for you?").
Acknowledge User's Environment: Mention that their IDE or documentation tools might have specific integrations, and you will defer to their preferred tool if your primary recommendation isn't suitable (e.g., "If your IDE isn't set up for PlantUML, we can use Mermaid, though it might offer slightly less detail for this type of UML diagram.").
Proceed only after user confirmation or selection.

4. Based on the confirmed diagram type and tool, internally define or select an appropriate JSON schema. 
This schema must capture all necessary elements of the implementation plan you intend to visualize (nodes, actors, states, classes, their properties, relationships, messages, transitions, conditions, loops etc.).  
This is an internal step for you to structure the data logically before translation.

5. Internally Generate the JSON Object: Translate the relevant parts of your implementation plan into the JSON structure defined in Step 4. Focus on accurately representing the semantics, logic, and relationships of the plan within the JSON object.

6. Internally Validate and Refine the JSON Object:  Validate your generated JSON against the schema from Step 4 to ensure structural correctness. 
Review the JSON internally to confirm it accurately reflects the implementation plan details you intend to convey. 
If there are errors or inaccuracies, refine your internal JSON generation logic and repeat Step 5.

7. Convert Validated JSON to Target Diagram Syntax:  Using your internal coding capabilities, parse the validated JSON object. 
Translate this JSON data into the precise, syntactically correct code for the diagramming tool confirmed by the user in Step 3.    
Ensure your conversion logic adheres strictly to the syntax rules, conventions, and version of the chosen diagramming tool to prevent rendering errors.

8. Apply Diagramming Best Practices During Conversion:
Labels: Generate clear, concise, and meaningful labels for all diagram elements (nodes, edges, actors, states, messages, etc.) based on the information in your JSON.    
Layout Optimization:
If the chosen tool supports layout directives (e.g., graph TD in Mermaid , rankdir=LR in Graphviz ), include these in the generated syntax to optimize for readability (e.g., top-to-bottom or left-to-right).   
Structure the elements in your JSON and conversion logic in a way that naturally leads to a clear layout, minimizing crossed lines and visual clutter, even when relying on the tool's automatic layout engine.    
Styling and Colors: If using colors or specific styles, ensure they enhance readability and understanding. Prioritize good color contrast for accessibility.    
Comments (Optional): If the diagramming language supports comments, consider adding them to the generated syntax for particularly complex parts of the diagram, derived from your internal plan notes.  

9. Present the Diagram Syntax/Rendered Diagram to the User:
Provide the generated diagram syntax to the user as part of your implementation plan explanation.
If you have the capability to render the diagram (e.g., if the user's environment supports it directly, or via an API call to a rendering service like Kroki ), present the visual diagram.   
Explain how the diagram illustrates the specific part of the implementation plan.
Be prepared to iterate based on user feedback, which might involve revisiting earlier steps (e.g., choosing a different diagram type, refining the details in the JSON, or adjusting the conversion logic).
