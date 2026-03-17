# AutoFill / Syntex Design

## Role

AutoFill and Syntex are the first processing step that transforms invoice files into structured data on SharePoint.

The information extracted at this stage becomes the prerequisite for subsequent Agent ① and Agent ②.

## Expected Responsibilities

### AutoFill

- Invoice Number extraction
- Issue Date extraction
- Due Date extraction
- Total Amount extraction
- Bill To Name extraction

### Syntex

- Verify presence of required fields
- Detect missing values or anomalies
- Determine processing completion
- Establish the trigger condition for Agent ①

## Design Thinking

- Do not assume manual user input
- However, do not auto-confirm completely — design to route to human review
- Treat together with SharePoint column design so extraction results are immediately displayable in list view

## Relationship with Agents

- Agent ① is not triggered until AutoFill / Syntex completes
- Extraction failures or anomalies are routed to Human Review
- Processing results are reflected in the SharePoint status column

## Notes

- Actual model definition: out of scope for this submission
- Training data conditions: out of scope for this submission
- Trigger condition detailed spec: covered in video demo
