## Análisis de Facturación Adidas 2020-2021

Este proyecto tuvo como objetivo principal implementar herramientas de Inteligencia de Negocios (*Business Intelligence*) y análisis de datos a gran escala para estudiar el comportamiento de la facturación de Adidas en Estados Unidos durante los años 2020 y 2021. 

El propósito es identificar *insights* o patrones clave que permitan a la compañía implementar estrategias de crecimiento, predecir tendencias en productos, fechas y zonas, y reforzar la fuerza de ventas.

La ejecución se basó en el uso de dos herramientas tecnológicas fundamentales: **SQL Server** para la gestión de datos y **Microsoft Power BI** para el análisis y la visualización.

---
La herramienta **SQL Server Management Studio** fue esencial para la etapa de preparación de datos y modelado.

* **Origen de Datos y Levantamiento:** SQL Server se utilizó para el levantamiento de los archivos CSV originales que componían el *Dataset* de facturación.
* **Base para el Modelado:** La base de datos relacional creada en SQL Server sirvió como fuente de datos principal para el análisis. El modelo inicial se estructuró con una tabla de Hechos (`VENTAS`) y diez (10) tablas de Dimensiones.
* **Conexión con Power BI:** La información de las 11 tablas del *Dataset* se importó, estableciendo una conexión directa para el posterior análisis en Power BI.

## Conceptos de Data Analytics Aplicados

El proyecto siguió un proceso estructurado de análisis de datos:

1.  **Limpieza y Transformación de Datos (ETL):** * Manejo de valores nulos, duplicados e incoherentes.
    * Transformación de datos, incluyendo cambios en nombres de columnas y aplicación de lógica condicional (ej. en la tabla `Región`).
2.  **Modelado de Datos:** Creación de las tablas de Hechos y Dimensiones con relaciones claras y coherentes (Modelo Estrella) dentro de Power BI para un análisis eficiente.
3.  **Hipótesis de Negocio:** Se trabajaron hipótesis como la influencia del tipo de venta con las estaciones, el potencial de facturación por regiones (Florida, New York, California) y la rentabilidad vs. unidades vendidas.
4.  **Definición de Métricas:** Elaboración y cálculo de métricas clave en materia financiera (metas de ventas, utilidades esperadas) y operacionales (movimiento de inventario por unidades facturadas).

---

## Herramientas Principales de Power BI

**Power BI** fue la herramienta central para la generación de tableros, visualizaciones y análisis dinámicos.

### 1. Medidas (DAX - Data Analysis Expressions)

Las medidas son cálculos dinámicos esenciales para la Inteligencia de Negocios, que cambian su resultado según los filtros aplicados en el informe.

* **Creación de la Tabla Calendario:** Se utilizó la función DAX `CALENDARAUTO()` para generar una tabla de fechas (`CALENDARIO`), esencial para el análisis por periodos (Año, Mes, Trimestre).
* **Medidas Financieras y Operacionales:** Se crearon medidas clave como:
    * `Total Facturado` y `Rentabilidad Total`.
    * `Volumen` (para contar las unidades vendidas).
    * Medidas de Tendencia Central: `Facturación Promedio`, `Rentabilidad Promedio`, `Facturación Mediana`, `Primer Cuartil` y `Tercer Cuartil`.
* **Medidas Narrativas:** Implementación de medidas para generar texto dinámico que resume los *insights* o patrones encontrados en función de los filtros seleccionados.

### 2. Filtros (Slicers)

* **Implementación:** Se implementaron múltiples filtros (*slicers*) para segmentar la información por categorías clave como **Categoría**, **Género**, **Región**, **Familia** y **Color**.
* **Interactividad:** Permiten a los usuarios restringir la información para realizar análisis detallados y dirigidos, facilitando la extracción de *insights* significativos.

### 3. Otras Herramientas Clave

* **Visualizaciones:** Uso de gráficos de **Barras**, **Mapas**, **Gráficos de Líneas** y **Tablas/Matrices** para transformar datos complejos en información gráfica y accesible.
* **Botones y Navegación:** Utilización de **Botones** y un **Navegador de Páginas** para crear una navegación intuitiva y fluida entre las diferentes hojas del informe.
* **Marcadores:** Asignación de un **Marcador** en la hoja principal para permitir a los usuarios *resetear* todos los filtros y selecciones con un solo clic.
* **Tooltips (Informes de Hoja de Información sobre Herramientas):** Creación de una hoja específica que actúa como una ventana emergente, mostrando información detallada (ciudades, ventas, rentabilidad, volumen) al posicionar el cursor sobre los estados en la visualización del mapa.

---

**Conclusión:** Este proyecto de Data Analytics proporciona al equipo ejecutivo una base sólida para la toma de decisiones estratégicas, permitiendo fundamentar acciones en el comportamiento histórico de la facturación para maximizar las utilidades.
