# Prompt 04 — Executive Readiness Review

**Reviewer Role:** Chief Financial Officer
**Date:** December 2024
**Package Under Review:** Post-Acquisition Vendor Spend Analysis

---

## Executive Readiness Verdict

**READY WITH MINOR REVISIONS**

---

## Strengths

- **Materiality focus is correct.** The Top 3 opportunities target $4.5M of the $7.9M total spend (57%), appropriately ignoring long-tail noise. Salesforce alone represents 39% of spend—this is the right place to start.

- **Conservative savings estimates.** The 10–15% range for Salesforce and 15–20% for workspace are at the lower end of industry benchmarks. This is appropriate for pre-close analysis without utilization data.

- **Clear execution timeline.** The 30/60/90 day framework is practical and assigns appropriate urgency (travel consolidation first as low-hanging fruit, Salesforce and workspace requiring more diligence).

- **QC process is documented.** The QC pass identified 22 flagged vendors including near-duplicates and encoding issues. No classification changes were required, indicating initial pass was sound.

- **Hedged language throughout.** Descriptions appropriately use "likely," "appears," and "typically" where inference was required from vendor names alone.

- **Memo is executive-appropriate.** Under one page, bottom-line-up-front structure, actionable recommendation. A CEO could read this in 2 minutes and make a decision.

- **No customer/revenue risk.** All three opportunities target internal operations—this is critical for post-acquisition credibility.

---

## Risks or Gaps

- **Methodology documentation is incomplete.** The `methodology.md` file in the repository is empty. For a submission package, this should explain the analytical approach, AI tool usage, and prompt design. This is a rubric requirement.

- **Salesforce savings assumption is aggressive at the high end.** While 10% is conservative, 15% ($470K) may be optimistic without visibility into contract renewal timing or termination flexibility. Recommend narrowing to 10–12% or adding explicit caveat about contract lock-in.

- **Workspace savings depend on integration headcount decisions.** The memo states "no risk to customer operations" but workspace consolidation could affect employee experience. Consider softening to "minimal operational disruption" pending integration planning.

- **No mention of Support or SaaS departments.** The classification includes these as valid departments per Config, but no vendors were assigned. This is likely correct (no matching vendors) but could prompt a question—consider a footnote in methodology.

---

## Recommended Improvements

1. **Populate `methodology.md`** with a brief explanation of:
   - Analytical approach (spend-weighted classification, conservative inference from vendor names)
   - AI tool usage (Claude Code operating on repository files)
   - Prompt structure (01 Classification → 01b QC → 02 Opportunities → 03 Memo)
   - Quality control process (duplicate detection, encoding review, spend-tier validation)

2. **Tighten Salesforce savings range** to $310K–$400K (10–12%) or add explicit caveat: "Upper bound assumes contract renewal within 12 months."

3. **Minor memo edit:** Change "no risk to customer operations" to "no direct impact to customer-facing systems" for precision.

---

## Final Assessment

**Would I approve this for submission in a real acquisition diligence process?**

**Yes, with the methodology documentation added.**

The analytical work is sound. Vendor classifications are reasonable given the name-only constraint. The Top 3 opportunities are material, non-overlapping, and appropriately conservative. The executive memo is well-structured and actionable.

The missing methodology documentation is the only substantive gap. In a real diligence context, the acquiring company's finance team would want to understand how the analysis was conducted—particularly given AI tool usage. This is a 15-minute fix.

The package demonstrates:
- Executive judgment in prioritizing material spend over exhaustive analysis
- Appropriate conservatism in savings estimates
- Clear communication suitable for CEO/CFO consumption
- Quality control rigor

**Recommendation:** Add methodology documentation, then submit.

---

## Next Step

The package is **ready for submission after one revision**:

→ Populate `/methodology.md` with analytical approach, AI usage, and QC process documentation.

No changes required to the executive memo or opportunity analysis—these meet the executive readiness bar.
