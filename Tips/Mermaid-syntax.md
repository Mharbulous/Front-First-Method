This file serves as a reference for common Mermaid syntax errors encountered when working with Large Language Models (LLMs). It provides examples of error messages from GitHub, the underlying cause of the error, and the corresponding corrected syntax.

| Git Hub Error message | Example Cause of Error | Example Correction |
|---|---|---|
| Unable to render rich display<br><br>...lass Version version endPhase1_6<br>-----------------------^<br>Expecting 'SEMI', 'NEWLINE', 'EOF', 'AMP', 'COLON', 'DOWN', 'DEFAULT', 'NUM', 'COMMA', 'NODE_STRING', 'BRKT', 'MINUS', 'MULT', 'UNICODE_TEXT', got 'SPACE' | `subgraph Phase1 ["Phase 1"]`<br>`        Phase1_1["Phase 1.1: Identify Product Requirements"] -->         class Version version  `<br>`    end` | `subgraph Phase1["Phase 1"]`<br>`        Phase1_1["Phase 1.1: Identify Product Requirements"] -->         class Version version  `<br>`    end` |
