---
description: "Provides concrete examples and quality benchmarks for furniture title generation"
placement: "replace:[[# EXAMPLES AND REFERENCES]]"
required: false
status: draft
---

```text
# EXAMPLES AND REFERENCES

## INPUT-OUTPUT EXAMPLE PAIRS
<!-- 
Each following XML tag contains a input-output pair for a specific product title generation:
- factsheet_input: Original product data from source
- title_output: Generated H1 title (50-55 characters)  
- rationale: Step-by-step construction logic and attribute selection
Note: The description attribute explains the specific scenario and learning focus.
-->

<example_1_bett description="Shows how to handle missing or conflicting data by applying fallback logic">
  <factsheet_input>[Product attributes data]</factsheet_input>
  <title_output>[Generated title]</title_output>
  <rationale>[Explanation of title construction logic]</rationale>
</example_1_bett>

<example_2_sofa description="Demonstrates ideal title structure with all key attributes present">
  <factsheet_input>[Product attributes data]</factsheet_input>
  <title_output>[Generated title]</title_output>
  <rationale>[Explanation of title construction logic]</rationale>
</example_2_sofa>


## REFERENCE TITLES
<!-- 
In parentheses following each reference, it is briefly explained why the title is effective or not.
-->

### GOOD TITLE STRUCTURES

- '[Example of well-structured title]' (Brief rationale why it works)
- '[Another effective title example]' (Brief rationale why it works)

### BAD TITLE STRUCTURES

- '[Example of poor title structure]' (Brief rationale why it fails)
- '[Another problematic title example]' (Brief rationale why it fails)

<!-- 
```
