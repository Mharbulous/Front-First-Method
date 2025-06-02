This file serves as a reference for common Mermaid syntax issues and best practices when working with Large Language Models (LLMs).

## Best Practices

1. **Edge labels with spaces and special characters:**  Use -->|Approved| instead for cleaner edge labels.
2. **Subgraph naming:** Subgraph IDs with spaces need to be handled properly. Use subgraph Phase1 ["Phase 1: Display Name"] format.
3. **Short descriptions** Very long text in nodes can cause rendering issues. Shorten longer longer descriptions while keeping the meaning clear.
4. **Parentheses vs brackets:** Mixed usage can sometimes cause issues. Standardized to use square brackets [] for process nodes and curly braces {} for decision nodes.
5.  **Quote handling:** Text with special characters, colons, or long phrases should be wrapped in quotes to prevent parsing errors.
6.  **Keep it concise:** Aim for clarity and simplicity in your diagrams. Avoid overly complex structures that can be difficult to read and maintain.
7.  **Maintain consistent indentation:** While not always strictly enforced by Mermaid, consistent indentation improves the readability of your diagram code.
8.  **Avoid trailing spaces:** Be mindful of trailing spaces, especially in class definitions, as they can lead to unexpected parsing errors.
9.  **Validate frequently:** Validate your Mermaid code often by asking user to report on whether the mermaid diagram is rendering properly, especially after making significant changes, to catch syntax errors early.
10. **Use the Troubleshooting Checklist:**  When errors are encountered, start by systematically running through the Troubleshooting Checklist.  Never try to debug mermaid diagrams without first running through the Troubleshooting Checklist (see below).


## Toubleshooting Checklist
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
