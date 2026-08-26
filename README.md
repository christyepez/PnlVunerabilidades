# PnlVunerabilidades — Power BI PBIP/PBIR

Panel gerencial para seguimiento de avance, riesgo y vulnerabilidades a partir del archivo `dataCloud_All_20020629_Amanda.xlsx`.

## Formato
- PBIP como proyecto Power BI.
- PBIR para la definición del reporte.
- TMDL para el modelo semántico.

## Fuente temporal
Durante construcción y pruebas se usa el Excel de ejemplo. La fuente productiva de SharePoint se concentra en una sola variable `SourceUrl` dentro de `FactProjects.tmdl` para facilitar el cambio posterior.

## Compatibilidad PBIR
`PnlVunerabilidades.Report/definition/report.json` usa schema `report/3.2.0` y mantiene únicamente propiedades compatibles. `exportDataMode` está definido como `AllowSummarized` y no se utiliza `showHiddenFields`, que no es válido dentro de `/settings` para este schema.

## Datos reales del ejemplo
- 789 registros efectivos
- 30 Resource Groups
- 501 recursos distintos
- RiskLevel: Low / Medium / High / Critical
- SLA_Compliance: On Time / Non-compliant
- Environment: Prod / Nom-Prod
