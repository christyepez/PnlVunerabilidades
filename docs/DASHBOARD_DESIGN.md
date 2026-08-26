# Diseño gerencial v4

## Principios

- Eliminar visuales sin datos o que dependan de `Progress`.
- Priorizar vulnerabilidades, SLA, aging, criticidad, recursos y tendencias.
- Usar filtros dropdown en la franja superior.
- Colocar KPIs críticos inmediatamente a la derecha de los filtros.
- Usar azul oscuro `#17365D` para barras y líneas.
- Evitar visuales duplicados.

## Resumen Ejecutivo

Filtros: Ambiente, Riesgo, Severidad, Responsable.

KPIs: Vulnerabilidades, Críticas, SLA Vencido, Resource Groups, Recursos, En Riesgo, Cumplimiento SLA, Aging Promedio, High + Critical.

Visuales: tendencia mensual de vulnerabilidades, vulnerabilidades por nivel de riesgo y tabla Top Resource Groups.

## Portafolio y Seguimiento

Filtros: Ambiente, Tipo de Recurso, Riesgo, Responsable.

KPIs: Resource Groups, Recursos, SLA Vencido.

Visuales: vulnerabilidades por Resource Group, evolución mensual y tabla de seguimiento.

## Riesgo y Vulnerabilidades

Filtros: Riesgo, Severidad, SLA, Ambiente.

KPIs: En Riesgo, Críticas, SLA Vencido.

Visuales: barras por riesgo, columnas por severidad, línea de SLA vencido en el tiempo y detalle de riesgo.

## Tendencias y Aging

Filtros: Ambiente, Riesgo, SLA, Resource Group.

KPIs: Aging Promedio, SLA Vencido, SLA On Time.

Visuales: vulnerabilidades detectadas por mes, aging promedio por mes, distribución por bandas de aging y tabla de mayor antigüedad.

## Detalle de Vulnerabilidades

Filtros: Ambiente, Riesgo, Severidad, Tipo de Recurso, Responsable, SLA.

Tabla operativa con Resource Group, Resource Name, tipo, vulnerabilidad, riesgo, severidad, aging, SLA, Owner, Implementer y fechas.
