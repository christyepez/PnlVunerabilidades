# PnlVunerabilidades — Power BI PBIP/PBIR

Panel gerencial Power BI para seguimiento de vulnerabilidades Azure, SLA, aging, riesgo y criticidad.

## Fuente temporal local

Durante la construcción el modelo usa:

`C:\Users\ChristianYepez\OneDrive\dataCloud_All_20020629_Amanda.xlsx`

La consulta se concentra en `FactProjects.tmdl`, de modo que posteriormente se puede reemplazar el origen por SharePoint conservando el modelo y los visuales.

## Modelo real del archivo

- 789 registros efectivos.
- 30 Resource Groups.
- 501 recursos distintos.
- Riesgo: Low / Medium / High / Critical.
- SLA: On Time / Non-compliant.
- Aging: `Vulnerability Age`.
- Fechas de tendencia: `FirstEvaluationDate` y mes derivado `Evaluation Month`.

## UI v4 gerencial

La revisión v4 elimina el diseño genérico basado en proyectos/avance y usa los datos efectivamente disponibles en el archivo:

- Filtros superiores en modo dropdown.
- KPIs críticos inmediatamente a la derecha de los filtros.
- Eliminados visuales dependientes de `Progress`, porque el archivo de referencia no contiene valores en esa columna.
- Nuevas medidas: `Resource Groups`, `Critical Vulnerabilities`, `High Critical Vulnerabilities` y `At Risk Vulnerabilities`.
- Nuevos campos derivados: `Evaluation Month` y `Age Band`.
- Tendencias mensuales con gráficos de línea.
- Barras y líneas estandarizadas en azul oscuro `#17365D`.
- Eliminados visuales duplicados y referencias obsoletas a `Open Findings` / `Closed Findings` como medidas.
- Filtrado de filas vacías por `ResourceGroup`, evitando el falso proyecto `(Blank)`.

## Páginas

1. Resumen Ejecutivo.
2. Portafolio y Seguimiento.
3. Riesgo y Vulnerabilidades.
4. Tendencias y Aging.
5. Detalle de Vulnerabilidades.

El proyecto se mantiene en formato PBIP + PBIR + TMDL para permitir versionamiento en Git.
