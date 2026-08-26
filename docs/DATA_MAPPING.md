# Data Mapping and Quality

## Source Columns

| Source field | Report label | Quality handling |
|---|---|---|
| ResourceType | Resource Type | Trim/Clean |
| ChangeRequest | Change Request | Missing → Not provided |
| ResourceGroup | Resource Group | Required; blank rows excluded |
| ResourceName | Resource Name | Required; blank rows excluded |
| RiskLevel | Risk Level | Trim + proper casing |
| Severity | Severity | Trim + proper casing |
| UserImpact | User Impact | Missing → Not provided |
| DisplayName | Vulnerability | Missing → Not provided |
| FirstEvaluationDate | First Evaluation Date | Date |
| StatusChangeDate | Status Change Date | Date |
| Vulnerability Age | Vulnerability Age | Integer |
| Description | Description | Missing → Not provided |
| RemediationDescription | Remediation | Missing → Not provided |
| SLA_Compliance | SLA Compliance | Trim |
| Owner | Owner | Lowercase; missing → Not assigned |
| Environment | Environment | `Nom-Prod` → `Non-Prod` |
| Status_code | Status | Trim |
| Última fecha: Date Report | Report Date | Renamed to `Date Report` |
| Progress | Progress | Nullable; unused in executive visuals because sample is empty |
| Implementer | Implementer | Missing → Not assigned |

## Derived Fields

- `ResourceKey`
- `Evaluation Month`
- `Age Band`: `0-30 days`, `31-60 days`, `61-90 days`, `>90 days`
- `Is Overdue`
- `Is At Risk`
- `Is Critical`

## Required-field Data Quality

The sample has complete values for `ResourceGroup`, `ResourceName`, `Owner`, `RiskLevel`, `Severity`, `SLA_Compliance`, `Environment`, and `Status_code` across all 789 effective rows.
