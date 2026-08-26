# Data Mapping — Vulnerability Management

## Archivo de referencia

`dataCloud_All_20020629_Amanda.xlsx`, hoja `Sheet1`.

- 20 columnas de origen.
- 789 registros con información efectiva después de eliminar filas vacías.
- 30 `ResourceGroup` distintos.
- 501 combinaciones `ResourceGroup + ResourceName`.

## Mapeo gerencial

| Campo origen | Uso en el panel |
|---|---|
| ResourceGroup | Agrupador de proyecto / portafolio |
| ResourceName | Recurso afectado |
| ResourceType | Tecnología / categoría del recurso |
| RiskLevel | Nivel de riesgo |
| Severity | Severidad / criticidad |
| SLA_Compliance | Estado SLA y determinación de vencimiento |
| Vulnerability Age | Aging del hallazgo |
| Owner | Responsable accountable |
| Implementer | Responsable de implementación/remediación |
| Environment | Prod / Non-Prod |
| Status_code | Estado de salud del hallazgo |
| FirstEvaluationDate | Fecha de primera evaluación |
| StatusChangeDate | Fecha de cambio de estado |
| Última fecha: Date Report | Fecha del corte/reporting |
| Progress | Avance de remediación |
| DisplayName | Nombre de la recomendación/vulnerabilidad |
| Description | Descripción del hallazgo |
| RemediationDescription | Acción correctiva recomendada |
| ChangeRequest | Change relacionado |
| UserImpact | Impacto al usuario |

## Compatibilidad PBIR

Para conservar los visuales desarrollados inicialmente, Power Query agrega aliases:

- `Project = ResourceGroup`
- `Project ID = ResourceName`
- `Status = Status_code`
- `Progress % = Progress`
- `Start Date = FirstEvaluationDate`
- `End Date = StatusChangeDate`
- `Risk = RiskLevel`
- `Criticality = Severity`
- `Last Update = Date Report`
- `Area = ResourceType`
- `Category = DisplayName`

`Is Overdue` se calcula desde `SLA_Compliance = Non-compliant`. `Is At Risk` combina incumplimiento SLA y niveles High/Critical. `Is Critical` se deriva de nivel Critical.

## Cambio a SharePoint

La consulta concentra el origen en `SourceUrl`. El cambio productivo debe modificar únicamente esta variable por la URL final de SharePoint, siempre que la estructura del archivo final mantenga estas 20 columnas.
