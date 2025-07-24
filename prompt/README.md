# Prompt Documentation & Guidelines



<RULES_FOR_AI>

# Formatting and Structure Requirements (Prompt-Lint)
All prompts and modules must follow these formatting and structure rules:
- Valid YAML frontmatter
- naming conventions
- 

## Frontmatter Requirements
Every prompt and module file must contain valid YAML frontmatter.

### For Prompts

```yaml
---
description: "Short description of the prompt"
arguments:
```

### For Modules

```yaml
---
description: "Short description of the module"
placement: "replace:[[# HEADING]]"  # Specifies where the module is inserted in the prompt
status: draft|review|ready
---
```

## File Naming Conventions

**Prompt files:**
- The prompt file must be named starting with `01-`, be lowercase, and end with `.prompt.md`.
  - Example: `01-title_generation.prompt.md`

**Module files:**
- A module file must be named starting with `02-` or a higher number, be lowercase, use underscores to separate words, and end with `.module.prompt.md`.
  - The numbering (e.g., `02-`, `03-`, `04-` ...) must reflect the order in which modules are inserted into the prompt.
  - Example: `02-examples_and_references.module.prompt.md`, `03-filtering.module.prompt.md`

## File Content Specifications
- After the `---` line of the YAML frontmatter, you must insert one empty line.
- All following module or prompt content must be enclosed in a Markdown code block to ensure safe copy-paste as follows:

    ---
    description: "Short description"
    field_n: "<value>"  # Placeholder for required fields
    ---
    <!-- Leerzeile -->
    ```
    Entire prompt or module here
    ```
    
</RULES_FOR_AI>


