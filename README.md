# Análisis de Caso Shark Tank - Evaluación de Región y Metas

## Resumen Ejecutivo

La conversión de ventas en la región ha mostrado una disminución del **-4.5%** respecto al año anterior, a pesar de contar con más fuerza de ventas. Utilizando **Power BI Desktop** y **DAX**, construí un modelo de datos y creé medidas calculadas para identificar las causas raíz y evaluar la factibilidad de las metas propuestas. Después de identificar que las mayores oportunidades de mejora están en el **PMNP (ticket promedio)** y la **retención de consultoras**, recomiendo que el equipo de gestión implemente los siguientes ajustes para aumentar las ventas:

1. Estrategias de incremento del PMNP (productos Gana+ y alto valor)
2. Programas de retención para mejorar el % Ret 6d6
3. Revisión de la meta de C14 para alinearla a la realidad de cada zona

---

## Problema de Negocio

Las ventas completadas son esenciales para esta región, ya que están directamente vinculadas a los ingresos. Los stakeholders de gestión han notado que la región tiene una **tasa de conversión menor** de lo esperado (basado en las metas vs ventas reales). ¿Cómo podemos determinar dónde están fallando las zonas y qué ajustes se deben hacer para mejorar el desempeño regional y evaluar si la meta propuesta para C14-2019 es alcanzable?


---

## Metodología

### 1. Modelado de Datos en Power BI
- Conexión directa a Power BI Desktop mediante herramientas de modelado
- Creación de relaciones entre tablas (Variables Venta, Otras Variables, Metas)
- Transformación de columnas para análisis temporal (Año, Número de Campaña, Etiqueta Campaña)

### 2. Creación de Medidas DAX
Desarrollo de **17 medidas calculadas** clave para el análisis:

**Medidas de Negocio:**
- `FdV Real`: Ventas reales totales
- `Total Activas`: Consultoras activas totales
- `Total Pedidos`: Pedidos realizados
- `% Actividad`: Ratio de consultoras que pasan pedido
- `PMNP`: Promedio del pedido por consultora
- `PEGs`: Consultoras en riesgo de egresar
- `Productividad por Activa`: Venta por consultora

**Medidas de Comparación:**
- `FdV Real C9-C13`: Ventas de campañas 9-13
- `FdV Real C13`: Ventas de última campaña
- `Meta C14 por Zona`: Meta propuesta filtrada por zona
- `Meta Total C9-C13 por Zona`: Meta acumulada filtrada
- `Gap Meta Venta por Zona`: Brecha entre meta y realidad
- `% Crecimiento Requerido C14`: % necesario para cumplir meta

**Medidas de Evaluación:**
- `Cumplimiento Meta Pedidos`: % de cumplimiento
- `Cumplimiento Meta Venta`: % de cumplimiento
- `Gap Meta Venta`: Diferencia absoluta

### 3. Visualizaciones Creadas
- **Gráficos de línea**: Evolución temporal de ventas, productividad y % actividad
- **Gráficos de barras**: Comparativos por zona, gap de meta
- **Tablas dinámicas**: Análisis de factibilidad de metas
- **Tarjetas KPI**: Indicadores principales de la región

---

## Habilidades Técnicas

**Power BI:**
- Modelado de datos relacional
- DAX avanzado (CALCULATE, FILTER, SELECTEDVALUE, DIVIDE)
- Medidas calculadas y columnas calculadas
- Visualización de datos
- Conexión mediante MCP (Model Context Protocol)

**DAX:**
- Funciones de contexto (CALCULATE, FILTER)
- Funciones de agregación (SUM, AVERAGE, DIVIDE)
- Funciones de tabla (SUMMARIZECOLUMNS, SUMMARIZE)
- Variables (VAR, RETURN)
- Funciones de fecha y filtrado


---

## Resultados y Recomendación de Negocio

### Hallazgos Principales

#### 📉 Situación General
- **Ventas 2019**: S/ 38,230,185 (-4.5% vs 2018)
- **Consultoras activas**: 13,842 promedio (+1.3% vs 2018)
- **% Actividad promedio**: 84.7% (muy por encima del benchmark de 40%)
- **PMNP promedio**: S/ 268 (-3.6% vs 2018)

#### ⚠️ Problemas Identificados

**Problema 1: Caída del PMNP (Ticket Promedio)**
- Variable afectada: **PMNP**
- Impacto: El ticket promedio cayó de S/ 278.5 (2018) a S/ 268.4 (2019)
- Consecuencia: Aunque hay más consultoras, cada una compra menos por pedido

**Problema 2: Productividad en descenso**
- Variable afectada: **Productividad por Activa**
- Impacto: Cada consultora vendió S/ 9.1 menos que en 2018
- Consecuencia: Más equipo pero menos resultados

**Problema 3: Retención deficiente**
- Variable afectada: **% Ret 6d6**
- Impacto: Solo 43-47% de consultoras nuevas llegan a 6 pedidos consecutivos
- Consecuencia: Más del 50% de las nuevas consultoras abandonan

**Problema 4: Zonas críticas**
- Zonas 252 y 254 con caídas de **-14.2%** y **-18.6%** respectivamente
- Son precisamente las zonas con mayor crecimiento requerido para C14

### 📊 Evaluación de la Meta Propuesta para C14

| Métrica | Valor |
|---------|-------|
| Zonas que deben crecer | 13 de 17 (76%) |
| Zonas que cumplen actualmente (C9-C13) | 4 de 17 (24%) |
| Crecimiento requerido promedio | 6.8% |
| Zona más exigida | 252 (+13.95%) |
| Zona menos exigida | 231 (-9.49%) |


### 💡 Conclusión

**NO recomiendo** aprobar la meta de C14 como está propuesta. Las razones son:

1. **El 76% de las zonas** necesitan crecer entre 2% y 14%, pero la tendencia regional es **negativa (-4.5%)**
2. **Las zonas más exigidas** (252, 254, 271) son las que **peor desempeño** tienen
3. **No hay evidencia** de recuperación en PMNP o productividad
4. **La base es inestable**: más del 50% de nuevas consultoras abandonan antes de 6 campañas

### ✅ Recomendaciones

Debido a que los mayores impactos vendrán de mejorar PMNP y retención, recomiendo:

**Acciones Inmediatas:**
1. **Incrementar PMNP**: Campañas de productos Gana+ y alto valor
2. **Reducir PEGs**: De 3,000 (C09) a menos de 2,000 por campaña
3. **Mejorar % Ret 6d6**: De 43-47% a mínimo 55% mediante programas de acompañamiento
4. **Enfoque especial** en zonas 252 y 254

**Revisión de Metas:**
- **Meta ajustada**: Crecimiento de 2-5% (no 7-14%) para las 13 zonas
- **Condición**: Implementar primero las acciones correctivas
- **Mantener meta actual** solo para las 4 zonas que ya están cumpliendo (211, 222, 231, 261)

Estas recomendaciones permitirán:
- ✅ Aumentar ventas de forma sostenible
- ✅ Mejorar la moral del equipo (metas alcanzables)
- ✅ Estabilizar la base de consultoras
- ✅ Recuperar productividad individual

---

## Próximos Pasos

### A Corto Plazo (1-2 meses)
1. ✅ **Implementar campañas de PMNP** en zonas piloto
2. ✅ **Programa de retención** para consultoras nuevas (primeros 6 pedidos)
3. ✅ **Monitorear PEGs** semanalmente

### A Mediano Plazo (3-6 meses)
1. 📊 **Medir impacto** de las acciones en PMNP y % Ret 6d6
2. 📈 **Recalibrar metas** de C15-C16 basadas en resultados reales
3. 🎯 **Plan de recuperación** específico para zonas 252 y 254

### A Largo Plazo (6-12 mesos)
1. 🔄 **Sistema de alertas tempranas** para detectar caídas como la de C09
2. 📚 **Base de conocimiento** de mejores prácticas por zona
3. 🎓 **Programa de capacitación** continua para nuevas consultoras


## Medidas DAX Principales

###  Gap Meta Venta por Zona
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

### % Crecimiento Requerido
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

###  % Actividad
```dax
% Actividad = 
DIVIDE(
    SUM('Variables Venta'[Pedidos]),
    SUM('Variables Venta'[Activas]),
    0
)


## Contacto y Contribuciones

- **Autor**: [Andres Johnson]
- **Fecha**: Febrero 2026

Si tienes preguntas sobre las medidas DAX, el modelado de datos o las conclusiones del análisis, no dudes en abrir un issue o contactarme directamente.

---

## Licencia

Este proyecto es parte de un caso de estudio académico y está disponible solo con fines educativos.
