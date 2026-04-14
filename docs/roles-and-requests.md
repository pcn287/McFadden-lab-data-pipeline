# Roles, contacts, and requesting new variables

## Teams

- **Team:** McFadden Lab Research Data Management  
- **Channel:** Data storage (workbook link, announcements, and how to get help)

Use that channel for **operational questions** about where to enter data and when the template was last updated.

---

## Requesting new variables (columns)

Students and staff should **not** silently add columns that the pipeline does not know about. Instead:

1. **Describe** the variable: name, definition, allowed values, units, and which study or protocol needs it.
2. **Post** the request in the **Data storage** channel (or follow the lab’s ticketing process if one exists).
3. **Wait for approval** from the data steward and/or Bovi-analytics so the **Template workbook**, **Teams** copy, and **pipeline** stay aligned.

After approval, the data steward updates **`Template workbook.xlsx`** (and the Teams copy), and Bovi-analytics updates **Databricks** expectations and **quality checks** as needed.

---

## Typical approvers

| Change | Who usually approves |
|--------|----------------------|
| New column or coding rule | Data steward + Bovi-analytics (pipeline impact) |
| New study block / study_id pattern | PI or delegated study lead + data steward |
| QC rule (validation logic) | Bovi-analytics + PI or delegate |

Exact names are filled in by the lab; this document is a **template** for governance text.
