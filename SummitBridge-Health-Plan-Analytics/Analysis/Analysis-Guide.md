# Analysis Workbook Guide

The file `SummitBridge-Health-Plan-Analysis.xlsx` contains the final analytical model and supporting output sheets.

## Workbook Sections

- **Executive Summary** — Strategic storyline, interventions and modeled opportunity.
- **External Benchmarks** — Directional comparison with published healthcare benchmarks.
- **README** — Workbook notes and navigation.
- **Member Spend** — Member-level cost, PMPM and high-cost segmentation.
- **Category Spend** — Allowed spend by service category and therapeutic area.
- **Avoidable ED** — ED classification, utilization and scenario calculations.
- **Behavioral Health** — Behavioral-health utilization and related ED patterns.
- **OON & Retention** — Out-of-network leakage, disenrollment and access signals.
- **Dashboard** — Workbook-based KPI summary.
- **Dataset Tabs** — Claims, member months, enrollment, providers and avoidable ED reference.

## Core Excel Logic

- `XLOOKUP` was used to enrich claims with member, provider and diagnosis-reference attributes.
- `SUMIFS` was used for member-level spend and exposure aggregation.
- PMPM was calculated as total allowed spend divided by total member months.
- High-cost members were identified using the 40th-largest member total because 5% of 800 members equals 40.
- Scenario models applied explicit adoption and optimization assumptions rather than claiming realized savings.

## Review Order

1. Executive Summary
2. Member Spend
3. Avoidable ED
4. OON & Retention
5. Dashboard
6. Underlying dataset tabs
