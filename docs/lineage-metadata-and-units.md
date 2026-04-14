# Provenance, audit metadata, and unit harmonization

This page names the ideas you asked for—**where data came from**, **who loaded or changed it**, **when**—and how **units** are made consistent in the pipeline.

---

## What to call “where, who, when” information

Different communities use overlapping terms; in practice you will use **more than one** of these together:

| Term | Plain-language meaning |
|------|------------------------|
| **Data provenance** | The **origin** and **history** of a dataset or row: which file, system, or study it came from, and how it was derived. |
| **Data lineage** | The **path** data take through systems (e.g., Teams workbook → Blob → Bronze → Silver → Gold), often shown as a graph or table. |
| **Audit trail** | **Who** did **what** **when**—especially for compliance: loads, updates, deletes, and approvals. |
| **Ingestion metadata** (or **operational metadata**) | Technical details captured **each time** data land in the lakehouse: job id, run time, source path, checksum, schema version, etc. |

In Azure/Databricks implementations, this information is usually stored as:

- **Columns** on curated tables (e.g., `ingested_at`, `source_file`, `pipeline_run_id`), and/or  
- **Separate logging / lineage** tables or tools (Unity Catalog lineage, job run history, application logs).

Bovi-analytics can choose the exact stack; this handbook states the **intent**: every promoted dataset should be **explainable** and **traceable**.

---

## What the pipeline should record (illustrative)

Examples of fields often attached at **ingest** or **publish** time (names are illustrative):

| Category | Example fields |
|----------|------------------|
| **Source** | Source system (e.g., SharePoint path, Blob URI), workbook version, sheet name |
| **Time** | `ingested_at`, `updated_at`, `pipeline_run_started_at` |
| **Actor** | Service principal or job name for automated loads; optional user id for manual publishes |
| **Versioning** | Template version, schema version, hash of source file |
| **Quality** | QC status, rule set version, quarantine reason (if any) |

Raw identifiers from Microsoft 365 (for example, exact user names) should follow **Cornell privacy and IT** policies; often **service accounts** and **run ids** are logged instead of student names unless policy allows.

---

## Uniform units and coding

**Silver / Gold** layers are where the lab enforces **one meaning per field** and **consistent units**:

- Map source units (e.g., lb, kg, g) to a **canonical unit** per variable.  
- Store **numeric value** and **canonical unit** (or unit as metadata in the variable dictionary).  
- Apply the same **coding** for categories (sex, treatment group) across studies where possible.

The **Instructions** sheet in `Template workbook.xlsx` and a **data dictionary** (maintained by the steward + Bovi-analytics) should stay aligned with what the pipeline enforces.
