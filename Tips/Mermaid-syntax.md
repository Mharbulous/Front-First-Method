This file serves as a reference for common Mermaid syntax issues and best practices when working with Large Language Models (LLMs).

## Best Practices

1.  **Keep it concise:** Aim for clarity and simplicity in your diagrams. Avoid overly complex structures that can be difficult to read and maintain.
2.  **Use meaningful IDs and names:** Choose descriptive IDs for nodes and classes to improve readability and understanding.
3.  **Maintain consistent indentation:** While not always strictly enforced by Mermaid, consistent indentation improves the readability of your diagram code.
4.  **Validate frequently:** Test your Mermaid code often, especially after making significant changes, to catch syntax errors early.
5.  **Avoid trailing spaces:** Be mindful of trailing spaces, especially in class definitions, as they can lead to unexpected parsing errors.

## Syntax Checklist
1. ### Trailing spaces
**Check for:** Trailing spaces on `class [node_id] [class_name]` lines, especially when immediately followed by `end` in a subgraph.

**Typical Error Message:** `Unable to render rich display ... Expecting 'SEMI', 'NEWLINE', 'EOF', 'AMP', 'COLON', 'DOWN', 'DEFAULT', 'NUM', 'COMMA', 'NODE_STRING', 'BRKT', 'MINUS', 'MULT', 'UNICODE_TEXT', got 'SPACE'`
#### Example of Incorrect Syntax
```
graph TD
    subgraph Example
        class Version version  
    end
```
#### Example of Correct Syntax
```
graph TD
    subgraph Example
        class Version version
    end
