# PnlVunerabilidades — Power BI PBIP/PBIR

Executive Power BI dashboard for vulnerability management, SLA compliance, aging, risk, severity, resources and operational follow-up.

## Current source
Local OneDrive file used for development:
`C:\Users\ChristianYepez\OneDrive\dataCloud_All_20020629_Amanda.xlsx`

## Report pages
1. Executive Summary
2. Portfolio Monitoring
3. Change Request Tracking
4. Risk & Vulnerabilities
5. Trends & Aging
6. Vulnerability Detail

## Data quality
The Power Query layer trims and cleans categorical text, normalizes `Nom-Prod` to `Non-Prod`, excludes empty records, and replaces missing business categories with `Unknown` or `Unassigned` to prevent `(Blank)` values in management visuals.

The model also includes `Data Quality Issues` and `Data Quality %` measures for governance.

## Change Request tracking
The report includes Change Request KPIs, descending CR distribution, a monthly CR vulnerability trend, and detailed CR-linked vulnerability tracking. `No aplica` is normalized to `Not Applicable`, and missing values to `Not Assigned`.
