# Prompt 01b — Vendor Classification Quality Control (QC)

## Objective

Perform a **quality control (QC) review** of the vendor classification output generated in Prompt 01.

This step is **not a re-classification exercise**.
It exists solely to ensure **consistency, correctness, and auditability** of the existing classifications.

---

## Scope & Constraints (MANDATORY)

### Data Scope

* Operate **only** on the classified vendor output produced by Prompt 01 and located in `/outputs`.
* **Do not** revisit or reinterpret the raw input file in `/data`.

### Analytical Constraints

You **must not**:

* Re-think vendor strategy
* Re-assign departments based on alternative logic
* Re-balance recommendations based on spend
* Apply new heuristics or frameworks

You **may only** make changes when a **clear, defensible issue exists**.

---

## Allowed QC Actions

You are permitted to perform **only** the following checks and corrections:

### 1. Duplicate Vendor Detection

* Identify exact or near-duplicate vendors (e.g., legal entity variants, capitalization differences).
* Merge duplicates **only when the vendor identity is clearly the same**.
* Preserve the **original classification logic** when merging.

### 2. Consistency Review

* Flag cases where:

  * The same vendor appears multiple times with different departments
  * Very similar vendors (e.g., same product/service class) are assigned conflicting departments or recommendations
* Correct inconsistencies **only if the discrepancy is clearly an error**, not a judgment call.

### 3. Obvious Misclassifications

You may correct classifications **only** when:

* The department is objectively incorrect (e.g., DocuSign not being G&A/Legal-adjacent)
* The recommendation conflicts with clearly identical peers (e.g., same SaaS tool treated differently without justification)

### 4. Data Quality Fixes

* Fix encoding issues, truncated vendor names, or formatting problems
* Normalize department naming where required (without inventing new departments)

---

## Change Control Rules (CRITICAL)

Every change **must**:

* Be minimal
* Be explicitly logged
* Include:

  * Vendor name
  * Original classification
  * Revised classification
  * Reason for change (1–2 lines, factual and non-speculative)

If no change is strictly required, **leave the record untouched**.

---

## Outputs Required

### 1. QC-Adjusted Dataset

* Save a **new file** in `/outputs`
* Append `_QC` to the original filename
* Do not overwrite the original Prompt 01 output

### 2. QC Change Log

* Provide a concise summary of:

  * Total records reviewed
  * Number of changes made
  * Categories of changes (duplicates, consistency, encoding, etc.)
* If no changes are made, explicitly state:
  **“QC review completed — no changes required.”**

---

## Final Instruction

This QC step is designed to **stabilize** the dataset, not improve it.

When in doubt:

> **Do not change the record.**

Do **not** proceed to any further analysis or prompts after completing this task.

