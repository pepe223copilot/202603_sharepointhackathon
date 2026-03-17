# 📊 SharePoint Hackathon 2026 — Build Your Own Copilot Cowork with SharePoint

> **Concept:** *Just Drop It* — Place your invoice. SharePoint and AI handle the rest: organizing, matching, approval prep, and CSV output.

---

## 🏆 Submission Categories

| Category | Our Angle |
|---|---|
| **Best organized library using Knowledge agent** | SharePoint designed as an AI grounding layer — business state managed via columns and views |
| **Best use of SharePoint in AI agents** | All agent inputs and outputs flow through SharePoint columns — end-to-end coherent design |

---

## 💡 Three Problems We Solve

| # | Before | After |
|---|--------|-------|
| 1 | Invoices arrive via email, downloads, and scans — scattered across locations | Auto-synced to SharePoint via OneDrive |
| 2 | Must open every file to check payee, amount, and due date | Syntex extracts columns — judge from the list view |
| 3 | Bank transfer CSV created manually each month | Agent ② auto-generates per-bank CSV on a monthly schedule |

---

## ⚙️ Full Processing Flow

```
📂 Local PC
   ↓ OneDrive sync
📄 SharePoint Document Library
   ↓ AutoFill / Syntex extracts invoice fields into columns
🤖 Agent ①  (auto-triggered on Syntex classification complete)
   ├─ Customer Master lookup → write CustomerID to SP column
   ├─ InvoiceApproval flow  (AI judgment via GPT-5.2 reasoning)
   └─ Sub-Agent writes Status + AICheckReason column, sends Teams notification
👤 Human final review  (update to HumanChecked)
🤖 Agent ②  (monthly schedule trigger)
   └─ Collect HumanChecked invoices → output per-bank CSV → update Status to Paid
```

---

## 📁 Repository Structure

```text
202603_sharepointhackathon/
├── README.md                              ← this file
├── docs/
│   ├── architecture.md                    ← overall architecture
│   ├── design-philosophy.md               ← Just Drop It philosophy
│   ├── category-fit.md                    ← category alignment
│   ├── agent-implementation-architecture.md ← implementation summary + InvoiceApproval flow spec
│   ├── presentation/                      ← slide HTML (8 slides, source)
│   └── sample/outputCSV/                  ← sample CSV output from Agent ②
presentation/
│   └── SharePointHackathon_Presentation.pdf  ← presentation PDF (final)
├── sharepoint/
│   ├── library-columns.md                 ← library column design (includes AICheckReason)
│   ├── views.md                           ← 6-view design
│   └── autofill-syntex/model-config.md    ← Syntex model configuration
└── masters/
    ├── customer-master-schema.md
    ├── billing-recipient-schema.md
    └── bank-master-schema.md

Note: Copilot Studio export files and environment-dependent workflow definitions are excluded from this public repository.
```

---

## 📎 Document Guide

| Purpose | Reference |
|------|---------|
| Overall flow and architecture | [docs/architecture.md](docs/architecture.md) |
| Just Drop It design philosophy | [docs/design-philosophy.md](docs/design-philosophy.md) |
| Category alignment explanation | [docs/category-fit.md](docs/category-fit.md) |
| Agent implementation summary and flow spec | [docs/agent-implementation-architecture.md](docs/agent-implementation-architecture.md) |
| Presentation (PDF) | [presentation/SharePointHackathon_Presentation.pdf](presentation/SharePointHackathon_Presentation.pdf) |
| Presentation (HTML source) | [docs/presentation/index.html](docs/presentation/index.html) |
| Team introduction | [docs/team.md](docs/team.md) |
| SharePoint column and view design | [sharepoint/](sharepoint/) |
| Master data schemas | [masters/](masters/) |
| Sample CSV output | [docs/sample/outputCSV/](docs/sample/outputCSV/) |