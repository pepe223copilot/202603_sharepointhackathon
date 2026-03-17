# Library Column Design

## Approach

The column design aims to enable business judgment without opening any invoice file.

AutoFill and Syntex extraction results, Agent matching results, and human review outcomes are all managed within the same library.

## Key Columns

### Invoice Basics

- Invoice Number
- Issue Date
- Due Date
- Total Amount
- Currency
- Bill To Name
- Supplier Name

### Matching Information

- CustomerID (looked up by Agent ① from Customer Master and written back)
- AICheckReason (judgment reason text from InvoiceApproval AI stage, written by Sub-Agent)
- Billing Recipient Match Result
- Match Confidence
- Validation Result
- Missing Field Flag

### Business Status Management

- Status (values: Unprocessed / AIChecked / AIRefused / HumanChecked / Paid)
- AICheckedStatus
- Output Target Month
- CSV Generation Status

### Supplementary Information

- Source Channel
- Uploaded By
- Sync Timestamp
- Model Name
- Notes

## What This Column Design Resolves

- Business judgment is possible even when file names are inconsistent
- Due date and status can be managed from a list view
- Agent inputs and outputs are traceable within SharePoint
- HumanChecked serves as a clear trigger for the next process step

## Operational Flow

- AutoFill extracts Invoice Number, Issue Date, Due Date, Amount, and Bill To
- Syntex detects missing required fields or anomalies
- Agent ① registers Customer ID
- Human confirms and sets Human Checked
- Agent ② updates CSV Generation Status

## Notes

- Column data types: out of scope for this submission
- Required settings and default values: out of scope for this submission
- Status transition formal definition: covered in video demo
