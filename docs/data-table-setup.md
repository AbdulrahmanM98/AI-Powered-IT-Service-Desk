# n8n Data Table setup

Create an n8n Data Table named `IT_Support_Tickets` before importing and running the workflows.

| Column | Type |
|---|---|
| ticket_id | String |
| employee_name | String |
| employee_email | String |
| teamviewer_id | String |
| issue_type | String |
| description | String |
| ai_summary | String |
| priority | String |
| sla_deadline | String |
| status | String |

Both workflows refer to this table by name. After import, check that **Save Ticket to Data Table**, **Find Ticket**, and **Update Ticket Status** are mapped to your newly created table.

Configure your own **OpenAI** and **Gmail** credentials in n8n; those bindings have been removed from the public exports. Replace the placeholder recipient `it.support@example.com` in **Notify Tech Team** with the address you actually want to receive alerts.

The original “Setup Data Table” workflow contained no nodes or table data. This document specifies the expected structure instead of publishing that empty workflow.

**Security note:** The original form uses employee names, email addresses and TeamViewer IDs. Use fake data when testing a public demo, and restrict access appropriately before any real-world deployment.
