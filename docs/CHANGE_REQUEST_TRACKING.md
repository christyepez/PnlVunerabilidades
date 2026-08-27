# Change Request Tracking

This page uses the existing, validated semantic-model measures and `ChangeRequest` as the analysis dimension.

Visuals:
- Change Request, Environment, Owner and SLA Compliance dropdown filters
- Vulnerabilities KPI
- Resources KPI
- SLA Non-Compliant KPI
- Vulnerabilities by Change Request, sorted descending
- Change Request Vulnerability Trend
- Change Request Detail table

All KPIs and charts respond to the Change Request slicer. This avoids introducing additional DAX measures solely for the page and keeps the report aligned with the stable semantic model.

Data quality:
- `No aplica` => `Not Applicable`
- blank ChangeRequest => `Not Assigned`
