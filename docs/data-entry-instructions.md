# General instructions for data entry (McFadden lab)

Read this **before** entering data in **`Template workbook.xlsx`**. The data steward may add lab-specific rules in the **Instructions** sheet of the workbook; when in doubt, those win.

---

## Core principles

1. **Use the template.** Do not maintain a parallel private spreadsheet for data that belong in the study record.
2. **Enter early, edit freely.** Excel for the web saves automatically; update rows when you correct mistakes—do not duplicate rows unless the protocol requires it.
3. **Stable identifiers.** Use the `study_id`, `subject_id`, and other IDs exactly as assigned—no extra spaces, consistent casing.
4. **One meaning per column.** Do not overload a column with multiple concepts; request a new variable if needed.
5. **Units and coding.** Put numeric values in numeric columns; put units in a dedicated unit column or follow the coding table in the Instructions sheet.
6. **Timestamps.** Use a consistent timezone convention (usually documented in the Instructions sheet); include date **and** time when the protocol requires it.
7. **Missing data.** Use the convention defined in the workbook (e.g., leave blank vs. explicit code); never use ambiguous placeholders like `-` unless defined.

---

## Before each session

- Confirm you are in the correct **study** row and **animal** row in the workbook.
- Confirm you have the latest link from the **Data storage** channel in Teams.

---

## After each session

- Skim for **obvious typos** in IDs and dates.
- If you changed the protocol or discovered a needed field, **request a template update** (see [roles-and-requests.md](roles-and-requests.md)) rather than hiding notes in free text that the pipeline cannot parse.

---

## Privacy and compliance

Follow Cornell and lab policies for **human subjects**, **animal protocols**, and **restricted data**. If unsure whether a field belongs in the shared workbook, ask the PI or data steward **before** entering it.
