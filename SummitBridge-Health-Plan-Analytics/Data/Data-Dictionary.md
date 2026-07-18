# Data Dictionary

## Claims

**Grain:** One claim line.

Key fields:

- `claim_id` — Claim-line identifier.
- `member_id` — Member identifier used for member-level aggregation.
- `rendering_npi` — Provider identifier.
- `service_date` — Date of service.
- `diagnosis_code_1` — Primary diagnosis used for condition and ED classification.
- `therapeutic_class` — Pharmacy therapeutic class where applicable.
- `billed_amount` — Provider charge before contractual adjustment.
- `allowed_amount` — Negotiated total cost recognized for the claim.
- `paid_amount` — Plan-paid component.
- `member_cost_share` — Member-paid component.
- `in_network_flag` — Network indicator.
- `service_category` — Inpatient, ED, PCP, Urgent Care, Specialty Rx or Behavioral Health.

## Enrollment

**Grain:** One member.

Key fields:

- `member_id`
- `line_of_business`
- `state`
- `county`
- `age`
- `risk_score`
- `attributed_pcp_npi`
- `disenrollment_reason`

## Member Months

**Grain:** One member-month.

Key fields:

- `member_id`
- `plan_id`
- `line_of_business`
- `state`
- `calendar_month`
- `member_months`

## Providers

**Grain:** One provider.

Key fields:

- `npi`
- `provider_type`
- `specialty_desc`
- `network_status`
- `quality_score`
- `panel_size`

## Avoidable ED Reference

**Grain:** One ICD-10 code.

Key fields:

- `icd10_code`
- `description`
- `avoidable_category`

Categories include Avoidable, Potentially Avoidable and Non-Avoidable.
