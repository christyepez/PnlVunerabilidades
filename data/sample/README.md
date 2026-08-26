# Sample data

El archivo temporal de referencia del proyecto es:

`dataCloud_All_20020629_Amanda.xlsx`

SHA-256 del archivo validado: `d9b226bd73385e7af193cebec16fd0ecc06e870dd5b1e8a5c8ffcafaf42c6a7d`.

Estructura validada: hoja `Sheet1`, 20 columnas de origen, 789 filas efectivas después de filtrar filas vacías.

El paquete distribuible `PnlVunerabilidades-PBIP.zip` incluye físicamente el XLSX bajo `data/sample/`. La consulta TMDL está preparada para apuntar a esta misma ruta publicada y posteriormente cambiar únicamente `SourceUrl` por la ubicación final de SharePoint.
