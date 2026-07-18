# Methodology

## Evidence Hierarchy

The analysis separates three types of statements:

1. **Observed findings** — Directly calculated from the supplied 2024 case data.
2. **Modeled scenarios** — Calculated using explicit adoption or optimization assumptions.
3. **Strategic inferences** — Recommendations that require pilots before causal or operational claims.

## Data Model and Joins

| Join | Purpose |
|---|---|
| Claims Member ID → Enrollment Member ID | Adds demographics, product line, risk and disenrollment fields |
| Claims Diagnosis Code → Avoidable ED Reference ICD-10 | Classifies ED claim lines |
| Enrollment Attributed PCP NPI → Providers NPI | Adds provider quality and network attributes |
| Member ID across Claims and Member Months | Aligns spend with exposure for PMPM and utilization rates |

## Core Formula Logic

- **Allowed Amount** = Paid Amount + Member Cost Share
- **PMPM** = Total Allowed Amount / Total Member Months
- **ED Claim Lines per 1,000** = ED Claim Lines / Member Months × 1,000
- **High-Cost Threshold** = 40th-largest member total allowed amount
- **OON Leakage Rate** = OON Allowed Amount / Total Allowed Amount
- **Strict ED Savings** = 20% × 613 × (Average ED Cost − Average Urgent-Care Cost)
- **Expanded ED Savings** = 20% × 914 × (Average ED Cost − Average Urgent-Care Cost)
- **Specialty Rx Savings** = Specialty Rx Allowed Amount × Optimization Percentage

## Analysis Modules

### Cost Concentration

Members were ranked by total allowed spend to identify top 1%, 5% and 20% cohorts.

### ED Utilization

ED claim lines were classified through an ICD-10 reference. Avoidable and potentially avoidable records formed a screening pool; clinical triage would be required before any redirection.

### Specialty Pharmacy

Spend was analyzed by drug and therapeutic class. Optimization scenarios were modeled at 5%, 10% and 15%.

### Retention and Access

Disenrollment was compared with PMPM, ED utilization, PCP access, OON utilization and high-cost status. Results were treated as associations and prioritization signals.

### Scenario Modeling

The cleanest direct scenarios were separated from broader strategic scenarios to avoid presenting unvalidated assumptions as a single business case.
