# Vendor Spend Strategy Analysis

This repository contains an AI-assisted vendor spend analysis conducted as part of a post-acquisition operational diligence exercise for an enterprise software company.

The objective of the analysis was to:
- Classify vendors by department
- Identify consolidation, optimization, and termination opportunities
- Surface the highest-impact cost-saving initiatives
- Produce an executive-level summary suitable for CEO/CFO review

Claude Code was used as an analytical assistant to operate directly on the files in this repository. All inputs, prompts, outputs, and methodology are included for transparency and reviewer inspection.

## Repository Structure & Artifacts

This repository is organized to allow full transparency into the analytical process and outputs used for executive decision-making.

- `/data/`  
  Raw vendor spend dataset provided as part of the assessment. All analysis is strictly based on vendor name and trailing 12-month spend.

- `/prompts/`  
  AI prompts used to guide vendor classification, quality control, and opportunity identification. These prompts define the analytical constraints and quality bar applied.

- `/outputs/`  
  Final analytical outputs produced from the classified data.

  - `vendor_classification_v1_QC.xlsx`  
    Primary analytical artifact used to derive executive recommendations, including department assignments, vendor descriptions, strategic recommendations, and QC annotations.

  - `top_3_cost_savings_opportunities.md` 
    Executive-ready summary of the three highest-impact cost-savings opportunities identified from the classified dataset.

- `methodology.md`  
  Description of the analytical approach, assumptions, constraints, and quality control steps applied.

- `QC.md`  
  Summary of secondary quality control review, including duplicate detection, encoding issues, and classification consistency checks.
