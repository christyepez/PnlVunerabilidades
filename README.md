# PnlVunerabilidades — Power BI PBIP/PBIR

Panel gerencial para seguimiento de vulnerabilidades, riesgo, SLA y avance de remediación a partir del archivo `dataCloud_All_20020629_Amanda.xlsx`.

## Estructura

- `PnlVunerabilidades.pbip`: punto de entrada del proyecto Power BI.
- `PnlVunerabilidades.Report`: definición PBIR del reporte.
- `PnlVunerabilidades.SemanticModel`: modelo semántico TMDL.
- `data/sample/dataCloud_All_20020629_Amanda.xlsx`: fuente temporal de referencia del proyecto.
- `docs`: diseño y mapeo de datos.

## Fuente de ejemplo

La estructura del modelo quedó alineada al archivo de referencia: 20 columnas de origen y 789 registros de vulnerabilidades con contenido (el Excel contiene además filas vacías que se filtran en Power Query).

Campos principales: `ResourceType`, `ChangeRequest`, `ResourceGroup`, `ResourceName`, `RiskLevel`, `Severity`, `UserImpact`, `DisplayName`, `FirstEvaluationDate`, `StatusChangeDate`, `Vulnerability Age`, `Description`, `RemediationDescription`, `SLA_Compliance`, `Owner`, `Environment`, `Status_code`, `Date Report`, `Progress` e `Implementer`.

El modelo mantiene además aliases gerenciales para conservar compatibilidad con los visuales PBIR existentes: `Project = ResourceGroup`, `Project ID = ResourceName`, `Risk = RiskLevel`, `Criticality = Severity`, `Start Date = FirstEvaluationDate` y `Last Update = Date Report`.

## Indicadores incorporados

- Proyectos / Resource Groups afectados.
- Total de vulnerabilidades.
- Recursos distintos afectados.
- Vulnerabilidades fuera de SLA.
- Vulnerabilidades On Time.
- % cumplimiento SLA.
- Aging promedio.
- Hallazgos abiertos/cerrados.
- Riesgo y criticidad.
- Ambiente Prod / Non-Prod.

## Cambio posterior a SharePoint

La partición `FactProjects` concentra la conexión en una sola variable `SourceUrl`. Durante la etapa de prototipo debe apuntar al archivo de muestra. Para producción únicamente se reemplaza `SourceUrl` por la URL final de SharePoint, manteniendo el resto de transformaciones, modelo y visuales.
