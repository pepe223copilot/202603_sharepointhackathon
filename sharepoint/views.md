# View Design

## Purpose

Views are used to understand the processing state of invoices without opening files.

The focus is on maintaining a flat library structure while enabling perspective switching based on the purpose of the viewer.

## Planned Views

### 1. New Intake View

- Review newly arrived invoices
- Sort by Sync Timestamp descending
- Identify files where AutoFill has not yet completed

### 2. AI Checked View

- List invoices that have passed AutoFill / Syntex
- Review Missing Field Flag and Validation Result
- Identify candidates for Agent ① processing

### 3. Human Review View

- Filter items with low Match Confidence
- Aggregate items where Billing Recipient Match Result requires review
- Human performs approval or rejection decision

### 4. Human Checked View

- List approved invoices
- Visualize the input set that Agent ② references

### 5. Payment This Month View

- Filter invoices where Due Date falls in the current month
- Show only Human Checked = Yes
- Verify targets for per-bank CSV generation

### 6. Error / Exception View

- Missing required fields
- Anomaly detection
- Master matching failure

## Design Intent

- Represent business stages via views, not folders
- Make the list alone sufficient to know what action is needed next
- Narrow down human review targets to reduce confirmation effort

## Notes

- Filter expression details: out of scope for this submission
- Sort order and grouping details: out of scope for this submission
- Conditional formatting rules: out of scope for this submission
