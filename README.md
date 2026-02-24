## Resumen Ejecutivo

La conversión de ventas ha sido baja en la región analizada, y necesitamos determinar la causa raíz y posibles soluciones. Usando **Power BI Desktop** y **DAX**, extraje datos del modelo y creé un dashboard completo con 17 medidas calculadas para rastrear el desempeño regional a través de múltiples dimensiones. Después de identificar que las mayores oportunidades están en mejorar el **ticket promedio por transacción** y la **retención de agentes**, recomiendo que el equipo de gestión implemente los siguientes ajustes que llevarán a una mayor conversión:

1. **Estrategias de incremento del ticket promedio** mediante productos premium
2. **Programas de retención** para agentes nuevos
3. **Revisión de metas** para alinearlas con la realidad de cada zona

---

## Problema de Negocio

Las transacciones completadas son esenciales para esta región, ya que están directamente vinculadas a los ingresos. Los stakeholders han notado que la región tiene una **tasa de conversión más baja** de lo esperado (basado en agentes activos vs ventas reales). ¿Cómo podemos determinar dónde están cayendo los agentes en el embudo de ventas y hacer ajustes estratégicos para motivarlos a completar más transacciones?

![dashboard-general](https://github.com/MundoG007/An-lisis-de-Inversiones-y-Negociaci-n-en-Power-BI/blob/main/dashboard-general.png.png?raw=true)

**Dashboard principal mostrando KPIs clave:** Ventas totales, variación año contra año, tasa de actividad y promedio de agentes activos. El gráfico de línea muestra la evolución mensual de ventas durante el periodo analizado, permitiendo identificar patrones y caídas significativas.

---

## Metodología

### 1. Consulta y modelado de datos en Power BI

Conecté directamente a Power BI Desktop mediante **MCP (Model Context Protocol)** y trabajé con el modelo de datos que contiene:

- **Tabla de Ventas**: Datos de transacciones, agentes activos, pedidos por periodo y zona
- **Tabla de Indicadores**: Métricas de retención, cobertura, tracción, tasa de conversión
- **Tabla de Metas**: Objetivos propuestos por periodo y zona

**Transformaciones aplicadas**:
- Creación de columnas calculadas para extraer año del periodo
- Conversión de tipos de datos para ordenamiento correcto
- Creación de etiquetas de periodo legibles (ej: "P01-2019")

### 2. Dashboard en Power BI que rastrea las métricas clave

Creé visualizaciones que permiten a los stakeholders ver:
- Evolución de ventas por periodo
- Comparativo año contra año (2018 vs 2019)
- Gap entre metas y ventas reales por zona
- Indicadores de productividad y actividad

### 3. Análisis de medidas DAX para simular cambios

Desarrollé 17 medidas calculadas estratégicas que permiten:
- Comparar desempeño actual vs metas
- Identificar zonas con oportunidades de mejora
- Calcular el crecimiento requerido para cumplir objetivos
- Evaluar la factibilidad de las metas propuestas

---

## Habilidades

**Power BI**: Modelado de datos, conexión MCP, visualizaciones, ETL, columnas calculadas

**DAX**: Medidas calculadas, funciones de contexto (CALCULATE, FILTER, SELECTEDVALUE), variables (VAR, RETURN), funciones de agregación (SUM, DIVIDE, AVERAGE)

**Análisis de Negocio**: Análisis de embudo de conversión, identificación de cuellos de botella, evaluación de KPIs, recomendaciones estratégicas

---

## Resultados y Recomendación de Negocio

Crear un dashboard para rastrear las ventas por zona da a los stakeholders visibilidad del embudo de conversión tanto a nivel general como por zonas específicas. Debido a democratizar estos datos, los stakeholders ahora pueden auto-servirse, y el equipo de analytics ahora tiene **menos solicitudes ad-hoc por semana**.

### Hallazgos Clave

Este análisis mostró que:

1. **Casi el 5% de ventas cayeron** vs el año anterior, a pesar de tener más agentes
2. **Menos del 25% de zonas** están cumpliendo sus metas actuales
3. **El ticket promedio cayó** por transacción, reduciendo ingresos a pesar de más actividad
4. **Más del 50% de agentes nuevos** abandonan antes de consolidarse


![analisis-problemas](https://github.com/MundoG007/An-lisis-de-Inversiones-y-Negociaci-n-en-Power-BI/blob/main/analisis-problemas.png?raw=true)

**Dashboard de análisis de problemas:** Muestra la evolución del ticket promedio por transacción, el porcentaje de actividad con línea de referencia al benchmark, agentes en riesgo de abandono por zona, y tabla de indicadores de retención. Esta vista permite identificar rápidamente las variables críticas que están afectando el desempeño regional.

### Impacto en Revenue

Según el modelo construido en Power BI:

- Aumentar el ticket promedio en **1%** resultará en **~$382K** más en ventas anuales
- Mejorar la retención en **1%** resultará en **~$280K** más en ventas anuales
- Reducir agentes en riesgo de 3,000 a 2,000 generará **~$500K** más por periodo

### Recomendaciones Estratégicas

Porque los mayores impactos probablemente vendrán de aumentar el ticket promedio y mejorar la retención, recomiendo algunos ajustes:

1. **Enviar recordatorios** a agentes inactivos para motivarlos a generar transacciones
2. **Trabajar con líderes de zona** para entrenar a los agentes y mostrarles el valor de productos premium
3. **Agregar comunicación clara** al inicio del proceso indicando que se tarda solo 5 min, y mostrar una barra de progreso para motivar completar el proceso
4. **Implementar programa de acompañamiento** para los primeros 6 periodos de agentes nuevos

Creo que estos ajustes abordarán los puntos críticos del embudo, **aumentarán la conversión y los ingresos**, y ahorrarán horas al equipo de analytics por reducción de solicitudes ad-hoc.

---

## Análisis Detallado

### a) Situación de la Región

**Ventas Totales 2019**: $38,230,185 (-4.5% vs 2018)

La región mostró una **tendencia de recuperación** a lo largo de 2019, pero con dos caídas críticas:

| Periodo | Ventas | Observación |
|---------|--------|-------------|
| P01 | $2,844,515 | Inicio del año |
| P07 | $3,411,069 | Primer pico |
| **P08** | **$2,948,037** | **Caída de -13.6%** |
| **P09** | **$3,000,701** | Recuperación parcial |
| P11 | $3,649,696 | Pico máximo |
| P12 | $3,657,044 | Máximo del año |
| P13 | $3,405,893 | Cierre |

**Comparativo 2018 vs 2019**:

| Indicador | 2018 | 2019 | Variación |
|-----------|------|------|-----------|
| Ventas Totales | $40,012,188 | $38,230,185 | **-4.5%** |
| Agentes (promedio) | 13,658 | 13,842 | **+1.3%** |
| Ticket Promedio | $278.5 | $268.4 | **-3.6%** |
| Productividad/Agente | $238 | $229 | **-3.8%** |
| % Actividad | 84.7% | 84.7% | Sin cambio |

**Conclusión**: La región tiene **MÁS agentes** pero vende **MENOS**. El problema es la **productividad individual**.

<img width="1306" height="732" alt="image" src="https://github.com/user-attachments/assets/0582a758-13be-4a8b-a03c-8de57e808be3" />
 
**Gráfico comparativo de ventas 2018 vs 2019:** Las dos líneas muestran la evolución periodo por periodo de ambos años. La línea de 2019 (azul) se mantiene consistentemente por debajo de 2018 (naranja), evidenciando una tendencia negativa a pesar del crecimiento en número de agentes. Los puntos de intersección revelan periodos específicos donde la brecha se amplió o redujo.

---

### b) Problemas Identificados

#### Problema 1: Caída del Ticket Promedio

- **Variable afectada**: Ticket Promedio por Transacción
- **Evidencia**: Cayó de $278.5 a $268.4 (-$10.1 por transacción)
- **Impacto**: Reduce ingresos directamente, aunque haya más agentes activos

**¿Por qué es un problema?**  
Aunque el % de actividad es alto (84.7%), si cada transacción vale menos, las ventas totales no crecen. Posibles causas:
- Menor poder adquisitivo de agentes
- Menos productos por transacción
- Bajo uso de productos premium

---

#### Problema 2: Productividad en Descenso

- **Variable afectada**: Productividad por Agente
- **Evidencia**: Cada agente generó $9.1 menos que en 2018
- **Impacto**: Paradoja - más equipo pero menos resultados

**Zonas críticas** (mayor caída 2019 vs 2018):

| Zona | Ventas 2018 | Ventas 2019 | Caída |
|------|------------|------------|--------|
| Z-254 | $1,966,373 | $1,601,275 | **-18.6%** |
| Z-252 | $2,116,513 | $1,815,969 | **-14.2%** |
| Z-261 | $2,670,989 | $2,434,741 | **-8.8%** |

---

#### Problema 3: Retención Deficiente

- **Variable afectada**: % Retención 6 periodos
- **Evidencia**: Solo 43-47% de agentes nuevos completan 6 periodos consecutivos
- **Impacto**: Más del 50% abandona antes de consolidarse

Esto explica por qué el equipo crece pero la productividad cae - alta rotación genera:
- Mayor esfuerzo en reclutamiento
- Menor experiencia promedio del equipo
- Pérdida de inversión en capacitación

---

#### Problema 4: Caída Puntual en P09

- **Variable afectada**: % Actividad (Periodo 09)
- **Evidencia**: Cayó a 78.3% (el más bajo del año), generando 3,003 agentes en riesgo
- **Impacto**: Pérdida de venta difícil de recuperar

---

### d) Evaluación de la Meta Propuesta

**Conclusión: NO es factible** en su forma actual.

#### Análisis de Cumplimiento

| Métrica | Valor |
|---------|-------|
| Zonas que **SÍ** cumplen meta actual | 4 de 17 (**24%**) |
| Zonas que **NO** cumplen meta actual | 13 de 17 (**76%**) |
| Zonas que deben **crecer** para siguiente periodo | 13 de 17 (**76%**) |
| Crecimiento promedio requerido | **+6.8%** |

<img width="1303" height="735" alt="image" src="https://github.com/user-attachments/assets/a43b50a7-4784-486a-8811-508f5b80be70" />

**Visualización del gap de metas por zona:** Las barras horizontales muestran la brecha entre el objetivo y la realidad actual. Las barras rojas (hacia la derecha) representan zonas que NO están cumpliendo sus metas y necesitarían crecer para alcanzarlas. Las barras verdes (hacia la izquierda) representan las únicas 4 zonas que SÍ están cumpliendo, donde incluso podrían reducir ventas y aún cumplir el objetivo. La línea vertical en cero sirve como punto de referencia para el cumplimiento exacto.

#### ¿Por qué NO es factible?

**Argumento 1: Tendencia regional negativa**  
La región cayó -4.5%, pero se pide que 76% de zonas crezcan entre 2% y 14%. No es realista sin acciones correctivas.

**Argumento 2: Zonas más exigidas = zonas más críticas**

| Zona | Caída 2019 vs 2018 | Crecimiento Requerido |
|------|--------------------|----------------------|
| Z-252 | **-14.2%** | **+13.95%** |
| Z-254 | **-18.6%** | **+11.13%** |
| Z-271 | **-1.0%** | **+9.92%** |

**Argumento 3: Ticket promedio sin recuperación**  
No hay evidencia de que el ticket promedio se recupere sin intervención.

**Argumento 4: Base inestable**  
Con 50%+ de abandono en primeros 6 periodos, la base es muy volátil.

---

## Tabla Detallada: Análisis por Zona

**<img width="507" height="422" alt="image" src="https://github.com/user-attachments/assets/bbf81633-bc12-4595-b6ff-8410ebdf3d4d" />
**  
 **Tabla de factibilidad de metas:** Presenta un análisis detallado zona por zona comparando las ventas reales del último periodo (P13) contra la meta propuesta para el siguiente periodo (P14). La columna de "% Crecimiento Requerido" muestra exactamente cuánto debe crecer cada zona para cumplir. Los íconos ✅ y ❌ indican visualmente el estado de cumplimiento, facilitando la identificación rápida de zonas problemáticas y exitosas.

| Zona | Ventas P13 | Meta P14 | Crecimiento Requerido | Estado |
|------|-----------|----------|----------------------|---------|
| Z-252 | $155,331 | $176,996 | **+13.95%** | ❌ |
| Z-254 | $127,142 | $141,297 | **+11.13%** | ❌ |
| Z-271 | $281,427 | $309,356 | **+9.92%** | ❌ |
| Z-212 | $210,201 | $229,273 | **+9.07%** | ❌ |
| Z-253 | $161,310 | $175,329 | **+8.69%** | ❌ |
| Z-111 | $262,450 | $283,274 | **+7.93%** | ❌ |
| Z-112 | $233,039 | $250,900 | **+7.66%** | ❌ |
| Z-223 | $205,369 | $219,949 | **+7.10%** | ❌ |
| Z-251 | $168,398 | $179,621 | **+6.66%** | ❌ |
| Z-255 | $220,689 | $233,665 | **+5.88%** | ❌ |
| Z-257 | $155,343 | $159,758 | **+2.84%** | ❌ |
| Z-221 | $161,725 | $165,329 | **+2.23%** | ❌ |
| Z-241 | $209,694 | $214,209 | **+2.15%** | ❌ |
| Z-261 | $195,188 | $189,980 | **-2.67%** | ✅ |
| Z-222 | $213,735 | $206,109 | **-3.57%** | ✅ |
| Z-211 | $172,542 | $163,730 | **-5.11%** | ✅ |
| Z-231 | $272,311 | $246,477 | **-9.49%** | ✅ |

---

## Medidas DAX Principales

### % Actividad
```dax
% Actividad = 
DIVIDE(
    SUM('Ventas'[Transacciones]),
    SUM('Ventas'[Agentes_Activos]),
    0
)
```
Calcula el ratio de agentes que generan transacciones. Benchmark: 40%. Región: 84.7% ✅

---

### Ticket Promedio
```dax
Ticket_Promedio = 
DIVIDE(
    SUM('Ventas'[Venta_Total]),
    SUM('Ventas'[Transacciones]),
    0
)
```
Valor promedio de cada transacción. Cayó de $278 a $268 ⚠️

---

### Gap Meta por Zona
```dax
Gap_Meta_Zona = 
VAR ZonaActual = SELECTEDVALUE('Ventas'[Zona])
RETURN
IF(
    NOT ISBLANK(ZonaActual),
    CALCULATE(
        SUM('Metas'[Meta_Venta]),
        'Metas'[Zona] = ZonaActual,
        'Metas'[Periodo] IN {"P09", "P10", "P11", "P12", "P13"}
    ) - 
    CALCULATE(
        SUM('Ventas'[Venta_Total]),
        'Ventas'[Zona] = ZonaActual,
        'Ventas'[Periodo] IN {"P09", "P10", "P11", "P12", "P13"}
    ),
    BLANK()
)
```
Brecha entre meta y realidad por zona. Positivo = no cumple, negativo = superó meta.

---

### % Crecimiento Requerido
```dax
Crecimiento_Requerido = 
VAR ZonaActual = SELECTEDVALUE('Ventas'[Zona])
VAR VentaP13 = CALCULATE(
    SUM('Ventas'[Venta_Total]),
    'Ventas'[Zona] = ZonaActual,
    'Ventas'[Periodo] = "P13"
)
VAR MetaP14 = CALCULATE(
    SUM('Metas'[Meta_Venta]),
    'Metas'[Zona] = ZonaActual,
    'Metas'[Periodo] = "P14"
)
RETURN
IF(
    NOT ISBLANK(ZonaActual) && VentaP13 <> 0,
    DIVIDE(MetaP14 - VentaP13, VentaP13),
    BLANK()
)
```
Porcentaje que debe crecer cada zona para alcanzar su meta del siguiente periodo.

---

### Agentes en Riesgo
```dax
Agentes_Riesgo = 
VAR Agentes_Totales = SUM('Ventas'[Agentes_Activos])
VAR Trans_Totales = SUM('Ventas'[Transacciones])
RETURN
    Agentes_Totales - Trans_Totales
```
Agentes activos que NO generaron transacciones (en riesgo de abandonar).

---

### Meta Acumulada por Zona
```dax
Meta_Acumulada_Zona = 
VAR ZonaActual = SELECTEDVALUE('Ventas'[Zona])
RETURN
IF(
    NOT ISBLANK(ZonaActual),
    CALCULATE(
        SUM('Metas'[Meta_Venta]),
        'Metas'[Zona] = ZonaActual,
        'Metas'[Periodo] IN {"P09", "P10", "P11", "P12", "P13"}
    ),
    BLANK()
)
```
Suma de metas para periodos específicos, filtrada por la zona seleccionada.

---

### Ventas Periodo Específico
```dax
Ventas_Periodos_Meta = 
CALCULATE(
    SUM('Ventas'[Venta_Total]),
    'Ventas'[Periodo] IN {"P09", "P10", "P11", "P12", "P13"}
)
```
Ventas reales para el periodo donde existen metas.

---

### Productividad por Agente
```dax
Productividad_Agente = 
DIVIDE(
    SUM('Ventas'[Venta_Total]),
    SUM('Ventas'[Agentes_Activos]),
    0
)
```
Venta promedio generada por cada agente activo.

---

### Ventas Totales Año
```dax
Ventas_Total_2019 = 
CALCULATE(
    SUM('Ventas'[Venta_Total]),
    'Ventas'[Año] = "2019"
)
```
Total de ventas del año 2019.

---

### Cumplimiento de Meta
```dax
Cumplimiento_Meta = 
DIVIDE(
    SUM('Ventas'[Venta_Total]),
    SUM('Metas'[Meta_Venta]),
    0
)
```
Porcentaje de cumplimiento de la meta de ventas.

---

## Próximos Pasos

### Corto Plazo (1-2 meses)
1. ✅ Implementar campaña de productos premium en zonas piloto
2. ✅ Programa de retención para agentes nuevos (primeros 6 periodos)
3. ✅ Monitorear agentes en riesgo semanalmente con dashboard en tiempo real

### Mediano Plazo (3-6 meses)
1. 📊 Medir impacto de acciones en ticket promedio y retención
2. 📈 Recalibrar metas con datos actualizados
3. 🎯 Plan especial de recuperación para zonas críticas (Z-252, Z-254)

### Largo Plazo (6-12 meses)
1. 🔄 Sistema de alertas tempranas para detectar caídas
2. 📚 Base de conocimiento de mejores prácticas
3. 🎓 Programa de capacitación continua certificado

---

## Conclusión

Los datos demuestran claramente que aunque la región tiene fortalezas (alto % de actividad, crecimiento en número de agentes), enfrenta desafíos críticos en productividad individual. La meta propuesta **no es alcanzable** sin implementar primero acciones correctivas en ticket promedio y retención. Recomiendo:

1. **Ajustar metas** a crecimiento de 2-5% (no 7-14%)
2. **Implementar acciones** de mejora de ticket promedio y retención
3. **Reevaluar** en 3 meses basado en resultados medibles

---

## Contacto

**Proyecto**: Análisis Regional de Ventas  
**Herramientas**: Power BI Desktop, DAX, MCP  
**Fecha**: 2019-2020

Para preguntas sobre medidas DAX, modelado o conclusiones, contacta directamente.

---

## Nota sobre los Datos

Los datos utilizados en este análisis fueron generados con IA y adaptados para propósitos demostrativos, manteniendo la estructura y patrones del análisis original.

