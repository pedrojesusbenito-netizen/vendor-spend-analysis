# Methodology

## Analytical Approach

This vendor spend analysis was conducted using a structured, prompt-driven methodology designed for conservative, defensible outputs suitable for CEO/CFO review.

### Data Inputs
- **Source:** Trailing 12-month vendor spend data (386 vendors, $7.89M total)
- **Available fields:** Vendor name and USD spend only
- **No external research** was performed; all inferences derived from vendor names

### Classification Framework

Vendors were classified using spend-weighted conservatism:

| Spend Tier | Threshold | Default Recommendation |
|------------|-----------|------------------------|
| High | >$100K | Optimize |
| Mid | $10K–$100K | Consolidate |
| Low | <$10K | Terminate (if non-core) |

Departments were assigned from a fixed list: Engineering, Facilities, G&A, Legal, M&A, Marketing, SaaS, Product, Professional Services, Sales, Support, Finance.

---

## AI Tool Usage

**Tool:** Claude Code (Anthropic)
**Mode:** Direct file operations within repository

Claude Code was used as an analytical assistant to:
1. Read and process the Excel vendor dataset
2. Apply classification logic systematically across 386 vendors
3. Generate structured outputs (classifications, opportunities, memos)
4. Perform quality control checks

All prompts, inputs, and outputs are preserved in the repository for transparency.

---

## Prompt Sequence

| Prompt | Purpose | Output |
|--------|---------|--------|
| 01 | Vendor classification | `vendor_classification_v1.xlsx` |
| 01b | Quality control pass | `vendor_classification_v1_QC.xlsx` |
| 02 | Top 3 opportunities | `top_3_cost_savings_opportunities.md` |
| 03 | Executive memo | `executive_memo_v3.md` |
| 04 | Readiness review | `executive_readiness_review.md` |

Each prompt built upon prior outputs. No prompt was executed until its upstream dependencies existed in the repository.

---

## Quality Control Process

### QC Checks Performed
1. **Duplicate detection:** Identified 5 near-duplicate vendor groups (e.g., Navan, AWS, Apple entities)
2. **Encoding validation:** Flagged 10 vendors with character encoding issues (source data artifacts)
3. **Spend-tier consistency:** Verified recommendation alignment with spend thresholds
4. **Department validation:** Confirmed all assignments from approved list
5. **Blank value check:** Identified 1 placeholder vendor ("Blank")

### QC Outcome
- **386 vendors reviewed**
- **0 classification changes required**
- **22 vendors flagged** for awareness (near-duplicates, encoding issues)
- **18 low-spend Optimize classifications** verified correct (essential services)

---

## Key Constraints Applied

- No assumptions beyond vendor name inference
- Hedged language where uncertainty exists ("likely," "appears to be")
- Conservative savings estimates (low end of industry benchmarks)
- No disruption to customer-facing or revenue systems
- All recommendations executable within 90 days post-close

---

## Reproducibility

All artifacts required to reproduce this analysis are contained in this repository:
- `/data/` — Source vendor spend file
- `/prompts/` — Task definitions and system instructions
- `/outputs/` — Generated classifications, analysis, and memos
