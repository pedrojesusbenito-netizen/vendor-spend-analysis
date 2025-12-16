# Task Prompt — Vendor Classification & Recommendation

## Objective

Classify each vendor in the provided vendor spend dataset as part of a post-acquisition operational diligence exercise. The goal is to produce **defensible, conservative, executive-grade classifications** suitable for CEO/CFO review.

You are acting as a **VP of Operations** supporting acquisition integration.

---

## Inputs

* Vendor dataset containing:

  * Vendor Name
  * Trailing 12-month spend (USD)

No other information is available.

---

## Required Outputs (Per Vendor)

Populate the following columns for **each vendor**:

1. **Department**
   Assign exactly one of the following:

   * Engineering
   * Product
   * Sales
   * Marketing
   * Support
   * Finance
   * Legal
   * G&A
   * Facilities
   * Professional Services
   * SaaS
   * M&A

2. **1-Line Vendor Description**

   * One concise sentence describing the vendor’s likely function
   * Use cautious language where appropriate (e.g., “likely,” “appears to be”)
   * Do **not** invent features or capabilities

3. **Strategic Recommendation**
   Choose exactly one:

   * **Optimize** — vendor is needed but cost, licensing, scope, or usage likely exceeds requirement
   * **Consolidate** — vendor overlaps with others providing similar services
   * **Terminate** — vendor appears non-essential, duplicative, or immaterial

---

## Classification Rules & Decision Framework

### Evidence Standard

* Base all decisions **strictly** on vendor name patterns and spend magnitude
* Do not use external research or unstated prior knowledge
* If the vendor’s function is unclear, state that explicitly in the description

### Spend-Weighted Conservatism

* High-spend vendors (>$100K):

  * Default to **Optimize**
  * Avoid Terminate unless clearly non-core
* Mid-spend vendors ($10K–$100K):

  * Favor **Consolidate** where overlap is plausible
* Low-spend vendors (<$10K):

  * Termination is acceptable if non-core or unclear

### Department Assignment Guidance

* Cloud infrastructure, developer tools → Engineering
* CRM, sales enablement → Sales
* Payroll, accounting, audit → Finance
* Recruiting, HR tools → G&A
* Offices, co-working, utilities → Facilities
* Agencies, consultants, auditors → Professional Services

When uncertain, choose the **most defensible** department and reflect uncertainty in the description.

---

## Output Quality Standards

* All fields must be populated
* Language must be professional and executive-appropriate
* Avoid marketing language or absolute claims
* Descriptions should be short, factual, and cautious
* Recommendations should reflect **post-acquisition rationalization logic**, not cost-cutting for its own sake

---

## Final Check Before Completion

Before finalizing:

* Review for internal consistency (similar vendors treated similarly)
* Ensure no obvious contradictions across recommendations
* Confirm tone and conservatism are appropriate for CEO/CFO review
