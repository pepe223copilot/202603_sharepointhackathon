# SharePoint Design

## Purpose

This directory organizes the SharePoint library design for invoice processing.

SharePoint is treated not as a storage location, but as the foundation that transforms invoices into business knowledge that AI can act upon.

## Expected Role of SharePoint

- Act as the destination for OneDrive sync
- Serve as the processing target for AutoFill / Syntex
- Hold extraction results, matching results, and approval status
- Serve as the reference foundation for Agent ① and Agent ②

## Design Scope

- Library column design
- View design
- AutoFill / Syntex design

## Why This Design Matters

To create a state where users can understand due dates, payees, amounts, approval status, and Customer ID at a glance — without ever opening a file.

## Notes

- Actual library name and URL: environment-specific, not included
- Permission scope and approver definitions: out of scope
- Boundary between SharePoint standard features and custom implementation: out of scope
