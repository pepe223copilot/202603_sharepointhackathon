# Model Configuration Notes

## Purpose

Notes for organizing AutoFill / Syntex model configuration items for invoice processing.

## Expected Configuration Items

- Model name
- Target document type: Invoice
- Extraction fields
- Required fields
- Output column for write-back
- Confidence threshold
- Status update content on completion

## Expected Extraction Targets

- Invoice Number
- Issue Date
- Due Date
- Total Amount
- Currency
- Bill To Name
- Supplier Name

## Expected Validation Items

- Due Date format validity
- Total Amount presence check
- Bill To Name extraction success
- All key columns populated

## Notes

- Model configuration details: out of scope for this submission
- Training accuracy and thresholds: out of scope for this submission
- Retraining operations: out of scope for this submission
