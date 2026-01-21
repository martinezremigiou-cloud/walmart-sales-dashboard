# Walmart Sales Dashboard (Google Sheets)

## Contexto
Análisis de ventas semanales de Walmart (2012) para evaluar desempeño por departamento y construir un resumen ejecutivo para stakeholders.

## Objetivo
Construir un dashboard ejecutivo con KPIs y visualizaciones para responder:
- ¿Qué departamentos son más eficientes? (Ventas por m²)
- ¿Qué departamentos contribuyen más al total? (Participación)
- ¿Qué tan estables/volátiles son las ventas por departamento? (Coeficiente de Variación)

## Estructura del archivo (tabs)
- raw_ventas: datos originales
- clean_ventas: datos limpiados y enriquecidos
- raw_departamento / raw_tiendas / Listas: tablas de referencia (lookups)
- Pivot: tablas dinámicas para KPIs
- Dashboard: visualizaciones + filtro dinámico
- Resumen: hallazgos e implicaciones
- README: documentación, KPIs y QA

## KPIs
- Ventas por m² (eficiencia): SUM(ventas) / AVG(tamaño_m2)
- Participación del departamento: ventas_depto / ventas_total
- Coeficiente de Variación (volatilidad): STDEV(ventas) / AVG(ventas)

## QA / Validaciones
- Tiendas sin departamento asignado: 0 (OK)
- Totales Pivot vs Raw: coinciden (OK)
- Ventas negativas o nulas: 27 registros detectados (hallazgo)
- Tamaño m² = 0: 0 (OK)
- CV razonable (< 2): OK

## Evidencia (capturas)
![Dashboard](Imágenes/validaciones.png)
![Resumen](Imágenes/resumen.png)
![KPIs y fórmulas](Imágenes/kpis-formulas.png)
![QA Validaciones](Imágenes/qa-validaciones.png)

## Entregables
- Archivo del proyecto (Excel): `Informes/Proyecto 2_ Resumen Ejecutivo de Ventas Walmart (1).xlsx`

## Próximos pasos
- Automatizar checks de QA y banderas de anomalías.
- Agregar tendencias (MoM/YoY) y alertas por volatilidad.
