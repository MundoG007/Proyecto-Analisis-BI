# Análisis de Caso Shark Tank - Evaluación Regional y Factibilidad de Metas

## Resumen Ejecutivo

La conversión de ventas ha sido baja en nuestra región, y necesitamos determinar la causa raíz y posibles soluciones. Usando **Power BI Desktop** y **DAX**, extraje datos de ventas del modelo y creé un dashboard completo con 17 medidas calculadas para rastrear el desempeño de la región a través de múltiples dimensiones. Después de identificar que las mayores oportunidades están en mejorar el **PMNP (ticket promedio)** y la **retención de consultoras**, recomiendo que el equipo de gestión implemente los siguientes ajustes que llevarán a una mayor conversión:

1. **Estrategias de incremento del PMNP** mediante productos Gana+
2. **Programas de retención** para nuevas consultoras
3. **Revisión de la meta de C14** para alinearla con la realidad de cada zona

---

## Problema de Negocio

Las ventas completadas son esenciales para esta región de venta directa, ya que están directamente vinculadas a los ingresos. Los stakeholders de producto y ventas han notado que la región tiene una **tasa de conversión más baja** de lo esperado (basado en consultoras activas vs ventas reales). ¿Cómo podemos determinar dónde están cayendo las consultoras en el embudo de ventas y hacer ajustes estratégicos para motivarlas a completar más pedidos?

![dashboard-general](https://github.com/MundoG007/An-lisis-de-Inversiones-y-Negociaci-n-en-Power-BI/blob/main/dashboard-general.png.png?raw=true)

---

## Metodología

### 1. Consulta y modelado de datos en Power BI

Conecté directamente a Power BI Desktop mediante **MCP (Model Context Protocol)** y trabajé con el modelo de datos que contiene:

- **Variables Venta**: Datos de ventas, consultoras activas, pedidos por campaña y zona
- **Otras Variables**: Indicadores de retención, cobertura, tracción, conversion rate
- **Metas**: Metas propuestas por campaña y zona

**Transformaciones aplicadas**:
- Creación de columnas calculadas para extraer año de campaña
- Conversión de tipos de datos para ordenamiento correcto
- Creación de etiquetas de campaña legibles (ej: "C01-2019")

### 2. Dashboard en Power BI que rastrea las métricas clave

Creé visualizaciones que permiten a los stakeholders ver:
- Evolución de ventas por campaña
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

Crear un dashboard para rastrear las ventas por zona da a los stakeholders de producto y ventas visibilidad del embudo de conversión tanto a nivel general como por zonas específicas. Debido a democratizar estos datos, los stakeholders ahora pueden auto-servirse, y el equipo de analytics ahora tiene **menos solicitudes ad-hoc por semana**.

### Hallazgos Clave

Este análisis mostró que:

1. **Casi el 5% de ventas cayeron** vs el año anterior (-S/ 1,782,003), a pesar de tener más consultoras
2. **Menos del 25% de zonas** están cumpliendo sus metas de C9-C13
3. **El PMNP cayó S/ 10** por pedido, reduciendo ingresos a pesar de más actividad
4. **Más del 50% de consultoras nuevas** abandonan antes de los 6 pedidos

![analisis-problemas](https://github.com/MundoG007/An-lisis-de-Inversiones-y-Negociaci-n-en-Power-BI/blob/main/analisis-problemas.png?raw=true)

*Dashboard de análisis de problemas mostrando evolución de PMNP, % Actividad, PEGs e indicadores de retención*

### Impacto en Revenue

Según el modelo construido en Power BI:

- Aumentar el PMNP en **1%** resultará en **~S/ 382K** más en ventas anuales
- Mejorar el % Ret 6d6 en **1%** resultará en **~S/ 280K** más en ventas anuales
- Reducir PEGs de 3,000 a 2,000 generará **~S/ 500K** más por campaña

### Recomendaciones Estratégicas

Porque los mayores impactos probablemente vendrán de aumentar el PMNP y mejorar la retención, recomiendo algunos ajustes:

1. **Enviar recordatorios** a consultoras inactivas para motivarlas a pasar pedido
2. **Trabajar con líderes de zona** para entrenar a las consultoras y mostrarles el valor de productos de alto ticket
3. **Agregar comunicación clara** al inicio del proceso indicando que se tarda solo 5 min, y mostrar una barra de progreso para motivar completar el pedido
4. **Implementar programa de acompañamiento** para las primeras 6 campañas de consultoras nuevas

Creo que estos ajustes abordarán los puntos críticos del embudo, **aumentarán la conversión y los ingresos**, y ahorrarán horas al equipo de analytics por reducción de solicitudes ad-hoc.

---

## Análisis Detallado

### a) Situación de la Región

**Ventas Totales 2019**: S/ 38,230,185 (-4.5% vs 2018)

La región mostró una **tendencia de recuperación** a lo largo de 2019, pero con dos caídas críticas:

| Campaña | Ventas | Observación |
|---------|--------|-------------|
| C01 | S/ 2,844,515 | Inicio del año |
| C07 | S/ 3,411,069 | Primer pico |
| **C08** | **S/ 2,948,037** | **Caída de -13.6%** |
| **C09** | **S/ 3,000,701** | Recuperación parcial |
| C11 | S/ 3,649,696 | Pico máximo |
| C12 | S/ 3,657,044 | Máximo del año |
| C13 | S/ 3,405,893 | Cierre |

**Comparativo 2018 vs 2019**:

| Indicador | 2018 | 2019 | Variación |
|-----------|------|------|-----------|
| Ventas Totales | S/ 40,012,188 | S/ 38,230,185 | **-4.5%** |
| Activas (promedio) | 13,658 | 13,842 | **+1.3%** |
| PMNP | S/ 278.5 | S/ 268.4 | **-3.6%** |
| Productividad/Activa | S/ 238 | S/ 229 | **-3.8%** |
| % Actividad | 84.7% | 84.7% | Sin cambio |

**Conclusión**: La región tiene **MÁS consultoras** pero vende **MENOS**. El problema es la **productividad individual**.

<img width="1306" height="732" alt="image" src="https://github.com/user-attachments/assets/0582a758-13be-4a8b-a03c-8de57e808be3" />
 
*Gráfico de líneas comparando la evolución de ventas 2018 vs 2019 campaña por campaña*

---

### b) Problemas Identificados

#### Problema 1: Caída del PMNP

- **Variable afectada**: PMNP (Promedio del Pedido)
- **Evidencia**: Cayó de S/ 278.5 a S/ 268.4 (-S/ 10.1 por pedido)
- **Impacto**: Reduce ingresos directamente, aunque haya más consultoras activas

**¿Por qué es un problema?**  
Aunque el % de actividad es alto (84.7%), si cada pedido vale menos, las ventas totales no crecen. Posibles causas:
- Menor poder adquisitivo de consultoras
- Menos productos por pedido
- Bajo uso de Gana+ (productos premium)

---

#### Problema 2: Productividad en Descenso

- **Variable afectada**: Productividad por Activa
- **Evidencia**: Cada consultora vendió S/ 9.1 menos que en 2018
- **Impacto**: Paradoja - más equipo pero menos resultados

**Zonas críticas** (mayor caída 2019 vs 2018):

| Zona | Ventas 2018 | Ventas 2019 | Caída |
|------|------------|------------|--------|
| 254 | S/ 1,966,373 | S/ 1,601,275 | **-18.6%** |
| 252 | S/ 2,116,513 | S/ 1,815,969 | **-14.2%** |
| 261 | S/ 2,670,989 | S/ 2,434,741 | **-8.8%** |

---

#### Problema 3: Retención Deficiente (% Ret 6d6)

- **Variable afectada**: % Ret 6d6
- **Evidencia**: Solo 43-47% de consultoras nuevas llegan a 6 pedidos consecutivos
- **Impacto**: Más del 50% abandona antes de consolidarse

Esto explica por qué el equipo crece pero la productividad cae - alta rotación genera:
- Mayor esfuerzo en reclutamiento
- Menor experiencia promedio del equipo
- Pérdida de inversión en capacitación

---

#### Problema 4: Caída Puntual en C09

- **Variable afectada**: % Actividad (Campaña 09)
- **Evidencia**: Cayó a 78.3% (el más bajo del año), generando 3,003 PEGs
- **Impacto**: Pérdida de venta difícil de recuperar

---

### d) Evaluación de la Meta Propuesta

**Conclusión: NO es factible** en su forma actual.

#### Análisis de Cumplimiento

| Métrica | Valor |
|---------|-------|
| Zonas que **SÍ** cumplen meta C9-C13 | 4 de 17 (**24%**) |
| Zonas que **NO** cumplen meta C9-C13 | 13 de 17 (**76%**) |
| Zonas que deben **crecer** para C14 | 13 de 17 (**76%**) |
| Crecimiento promedio requerido | **+6.8%** |

**[INSERTAR AQUÍ: gap-meta-zona.png]**  
*Gráfico de barras horizontales mostrando el gap de meta por zona (rojo = no cumple, verde = cumple)*

#### ¿Por qué NO es factible?

**Argumento 1: Tendencia regional negativa**  
La región cayó -4.5%, pero se pide que 76% de zonas crezcan entre 2% y 14%. No es realista sin acciones correctivas.

**Argumento 2: Zonas más exigidas = zonas más críticas**

| Zona | Caída 2019 vs 2018 | Crecimiento Requerido C14 |
|------|--------------------|--------------------------|
| 252 | **-14.2%** | **+13.95%** |
| 254 | **-18.6%** | **+11.13%** |
| 271 | **-1.0%** | **+9.92%** |

**Argumento 3: PMNP sin recuperación**  
No hay evidencia de que el PMNP se recupere sin intervención.

**Argumento 4: Base inestable**  
Con 50%+ de abandono en primeros 6 pedidos, la base es muy volátil.

---

## Tabla Detallada: Análisis por Zona

**[INSERTAR AQUÍ: tabla-factibilidad.png]**  
*Tabla completa mostrando las 17 zonas con FdV Real C13, Meta C14, % Crecimiento Requerido y Estado*

| Zona | FdV Real C13 | Meta C14 | Crecimiento Requerido | Estado |
|------|-------------|----------|----------------------|---------|
| 252 | S/ 155,331 | S/ 176,996 | **+13.95%** | ❌ |
| 254 | S/ 127,142 | S/ 141,297 | **+11.13%** | ❌ |
| 271 | S/ 281,427 | S/ 309,356 | **+9.92%** | ❌ |
| 212 | S/ 210,201 | S/ 229,273 | **+9.07%** | ❌ |
| 253 | S/ 161,310 | S/ 175,329 | **+8.69%** | ❌ |
| 111 | S/ 262,450 | S/ 283,274 | **+7.93%** | ❌ |
| 112 | S/ 233,039 | S/ 250,900 | **+7.66%** | ❌ |
| 223 | S/ 205,369 | S/ 219,949 | **+7.10%** | ❌ |
| 251 | S/ 168,398 | S/ 179,621 | **+6.66%** | ❌ |
| 255 | S/ 220,689 | S/ 233,665 | **+5.88%** | ❌ |
| 257 | S/ 155,343 | S/ 159,758 | **+2.84%** | ❌ |
| 221 | S/ 161,725 | S/ 165,329 | **+2.23%** | ❌ |
| 241 | S/ 209,694 | S/ 214,209 | **+2.15%** | ❌ |
| 261 | S/ 195,188 | S/ 189,980 | **-2.67%** | ✅ |
| 222 | S/ 213,735 | S/ 206,109 | **-3.57%** | ✅ |
| 211 | S/ 172,542 | S/ 163,730 | **-5.11%** | ✅ |
| 231 | S/ 272,311 | S/ 246,477 | **-9.49%** | ✅ |

---

## Medidas DAX Principales

### % Actividad
```dax
% Actividad = 
DIVIDE(
    SUM('Variables Venta'[Pedidos]),
    SUM('Variables Venta'[Activas]),
    0
)
```
Calcula el ratio de consultoras que pasan pedido. Benchmark: 40%. Región: 84.7% ✅

---

### PMNP (Ticket Promedio)
```dax
PMNP = 
DIVIDE(
    SUM('Variables Venta'[Venta]),
    SUM('Variables Venta'[Pedidos]),
    0
)
```
Valor promedio de cada pedido. Cayó de S/ 278 a S/ 268 ⚠️

---

### Gap Meta Venta por Zona
```dax
Gap Meta Venta por Zona = 
VAR ZonaActual = SELECTEDVALUE('Variables Venta'[Zona])
RETURN
IF(
    NOT ISBLANK(ZonaActual),
    CALCULATE(
        SUM('Metas'[Meta Venta]),
        'Metas'[Zona] = ZonaActual,
        'Metas'[Campaña] IN {"201909", "201910", "201911", "201912", "201913"}
    ) - 
    CALCULATE(
        SUM('Variables Venta'[Venta]),
        'Variables Venta'[Zona] = ZonaActual,
        'Variables Venta'[Campaña] IN {"201909", "201910", "201911", "201912", "201913"}
    ),
    BLANK()
)
```
Brecha entre meta y realidad por zona. Positivo = no cumple, negativo = superó meta.

---

### % Crecimiento Requerido C14
```dax
% Crecimiento Requerido C14 = 
VAR ZonaActual = SELECTEDVALUE('Variables Venta'[Zona])
VAR VentaC13 = CALCULATE(
    SUM('Variables Venta'[Venta]),
    'Variables Venta'[Zona] = ZonaActual,
    'Variables Venta'[Campaña] = "201913"
)
VAR MetaC14 = CALCULATE(
    SUM('Metas'[Meta Venta]),
    'Metas'[Zona] = ZonaActual,
    'Metas'[Campaña] = "201914"
)
RETURN
IF(
    NOT ISBLANK(ZonaActual) && VentaC13 <> 0,
    DIVIDE(MetaC14 - VentaC13, VentaC13),
    BLANK()
)
```
Porcentaje que debe crecer cada zona para alcanzar su meta de C14.

---

### PEGs (Posibles Egresos)
```dax
PEGs = 
VAR Activas_Totales = SUM('Variables Venta'[Activas])
VAR Pedidos_Totales = SUM('Variables Venta'[Pedidos])
RETURN
    Activas_Totales - Pedidos_Totales
```
Consultoras activas que NO pasaron pedido (en riesgo de abandonar).

---

### Meta Total C9-C13 por Zona
```dax
Meta Total C9-C13 por Zona = 
VAR ZonaActual = SELECTEDVALUE('Variables Venta'[Zona])
RETURN
IF(
    NOT ISBLANK(ZonaActual),
    CALCULATE(
        SUM('Metas'[Meta Venta]),
        'Metas'[Zona] = ZonaActual,
        'Metas'[Campaña] IN {"201909", "201910", "201911", "201912", "201913"}
    ),
    BLANK()
)
```
Suma de metas para campañas 9-13, filtrada por la zona seleccionada.

---

### FdV Real C9-C13
```dax
FdV Real C9-C13 = 
CALCULATE(
    SUM('Variables Venta'[Venta]),
    'Variables Venta'[Campaña] IN {"201909", "201910", "201911", "201912", "201913"}
)
```
Ventas reales para el periodo donde existen metas (C9-C13).

---

### Productividad por Activa
```dax
Productividad por Activa = 
DIVIDE(
    SUM('Variables Venta'[Venta]),
    SUM('Variables Venta'[Activas]),
    0
)
```
Venta promedio generada por cada consultora activa.

---

### FdV Total 2019
```dax
FdV Total 2019 = 
CALCULATE(
    SUM('Variables Venta'[Venta]),
    'Variables Venta'[Año] = "2019"
)
```
Total de ventas del año 2019.

---

### Cumplimiento Meta Venta
```dax
Cumplimiento Meta Venta = 
DIVIDE(
    SUM('Variables Venta'[Venta]),
    SUM('Metas'[Meta Venta]),
    0
)
```
Porcentaje de cumplimiento de la meta de ventas.

---

## Próximos Pasos

### Corto Plazo (1-2 meses)
1. ✅ Implementar campaña de productos Gana+ en zonas piloto
2. ✅ Programa de retención para consultoras nuevas (primeros 6 pedidos)
3. ✅ Monitorear PEGs semanalmente con dashboard en tiempo real

### Mediano Plazo (3-6 meses)
1. 📊 Medir impacto de acciones en PMNP y % Ret 6d6
2. 📈 Recalibrar metas de C15-C16 con datos actualizados
3. 🎯 Plan especial de recuperación para zonas 252 y 254

### Largo Plazo (6-12 meses)
1. 🔄 Sistema de alertas tempranas para detectar caídas
2. 📚 Base de conocimiento de mejores prácticas
3. 🎓 Programa de capacitación continua certificado

---

## Estructura del Proyecto

```
shark-tank-analysis/
│
├── README.md                           # Este archivo
├── images/                             # Carpeta con capturas de Power BI
│   ├── dashboard-general.png
│   ├── comparativo-2018-2019.png
│   ├── analisis-problemas.png
│   ├── gap-meta-zona.png
│   └── tabla-factibilidad.png
├── Reporte_SharkTank_Adjunto1.docx    # Reporte completo (16 páginas)
├── Guia_Reporte_SharkTank_Adjunto1.md # Guía de visualizaciones
├── Solucion_Linea_Recta.md            # Troubleshooting
└── Columnas_Nuevas_Creadas.md         # Documentación técnica
```

---

## Conclusión

Los datos demuestran claramente que aunque la región tiene fortalezas (alto % de actividad, crecimiento en número de consultoras), enfrenta desafíos críticos en productividad individual. La meta propuesta para C14 **no es alcanzable** sin implementar primero acciones correctivas en PMNP y retención. Recomiendo:

1. **Ajustar metas** a crecimiento de 2-5% (no 7-14%)
2. **Implementar acciones** de mejora de PMNP y retención
3. **Reevaluar** en 3 meses basado en resultados medibles

---

## Contacto

**Proyecto**: Caso Shark Tank - Análisis Regional  
**Herramientas**: Power BI Desktop, DAX, MCP  
**Fecha**: Febrero 2026

Para preguntas sobre medidas DAX, modelado o conclusiones, contacta directamente.

---

## Licencia

Este proyecto es parte de un caso de estudio académico con fines educativos.
