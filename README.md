# PnlVunerabilidades — Power BI PBIP/PBIR

Executive Power BI dashboard for vulnerability governance, remediation tracking, SLA compliance, aging and Azure resource exposure.

## Architecture

- **PBIP project**: `PnlVunerabilidades.pbip`
- **Report definition**: `PnlVunerabilidades.Report` using enhanced **PBIR**
- **Semantic model**: `PnlVunerabilidades.SemanticModel` using **TMDL**
- **Current source**: `C:\Users\ChristianYepez\OneDrive\dataCloud_All_20020629_Amanda.xlsx`
- **Future production source**: SharePoint/OneDrive; only the source step in `FactProjects.tmdl` must be replaced.

## Report Pages

1. **Executive Summary** — critical KPIs, vulnerability trend, risk distribution and top resource groups.
2. **Portfolio Monitoring** — resource-group exposure, monthly trend and operational portfolio monitoring.
3. **Risk & Vulnerabilities** — risk, severity, SLA non-compliance trend and risk detail.
4. **Trends & Aging** — detected vulnerabilities over time, average aging and aging distribution.
5. **Vulnerability Detail** — detailed operational table with dropdown filters.

## Core KPIs

- Total Vulnerabilities
- Resource Groups
- Distinct Resources
- Critical Vulnerabilities
- High + Critical Vulnerabilities
- At Risk Vulnerabilities
- SLA Non-Compliant
- SLA On Time
- SLA Compliance %
- Average Vulnerability Age
- Data Quality Complete %

## Data Quality Rules

The Power Query layer:
- excludes rows without `ResourceGroup` or `ResourceName`;
- trims and cleans text values;
- normalizes `Nom-Prod` to `Non-Prod`;
- normalizes risk and severity casing;
- converts missing descriptive values to `Not provided`;
- converts missing owner/implementer values to `Not assigned`;
- keeps the original `Progress` field nullable because the sample contains no populated values;
- derives `Evaluation Month` and `Age Band` in English.

## Current Data Profile

Based on the sample file:
- 789 effective vulnerability records;
- 30 resource groups;
- 501 distinct resources;
- required governance fields are complete for all effective rows;
- `Progress` is empty for all effective records and is intentionally not used in executive visuals.

## Open and Refresh

1. Keep the source workbook at `C:\Users\ChristianYepez\OneDrive\dataCloud_All_20020629_Amanda.xlsx`.
2. Open `PnlVunerabilidades.pbip` in Power BI Desktop.
3. Refresh the semantic model.
4. When the final SharePoint source is available, replace the local source step without changing the semantic layer or visuals.
