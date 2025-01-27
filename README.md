# Microsoft Fabric End2End. Análisis de Salud Mental en Comunidades Autónomas de España

Tuve el placer de participar en un proyecto End to End con Microsoft Fabric, nueva plataforma de Microsoft para soluciones de Big Data Analytics que integra todas sus herramientas previas. Se usaron datos del Ministerio de Salud español mediante su API. Se llevó a cabo un proceso ETL con PySpark con arquitectura Medallion y se realizó una visualización con Power BI.

A nivel práctico, este proyecto tuvo como objetivo analizar la relación entre la salud mental, el desempleo y la clase social en las comunidades autónomas de España. Utilizando herramientas de análisis de datos en la nube y visualización, se proporcionan insights clave para comprender cómo estos factores impactan en la población y cómo varían entre regiones.

## Descripción General

El análisis se centra en identificar patrones y tendencias relacionadas con la salud mental y las desigualdades socioeconómicas en España. El proyecto utiliza una arquitectura de datos basada en Microsoft Fabric, Power BI y técnicas de ETL (Extracción, Transformación y Carga) para procesar grandes volúmenes de datos provenientes de la API del Ministerio de Salud.

### Objetivos Específicos:
- Identificar las comunidades autónomas más vulnerables desde una perspectiva socioeconómica y de salud mental.
- Evaluar la correlación entre la tasa de desempleo y los problemas de salud mental.
- Analizar las disparidades de género en los riesgos de salud mental.

## Herramientas Utilizadas

- **Microsoft Fabric**: Plataforma de análisis de datos en la nube que integra almacenamiento, procesamiento y visualización en un solo entorno.
- **Power BI**: Herramienta de inteligencia de negocio utilizada para la visualización interactiva de datos.
- **Medallion Architecture**: Estructura basada en capas (Bronze, Silver, Gold) para la limpieza, procesamiento y análisis de datos.
- **PySpark**: Procesamiento paralelo y escalable de datos en la nube.
- **Delta Format**: Formato de almacenamiento para manejo eficiente de datos.

## Metodología

El proyecto sigue un enfoque ETL estructurado para garantizar la calidad y consistencia de los datos. Las fases principales son:

### Extracción
- Datos obtenidos de la API INCLANS del Ministerio de Salud.
- Fuentes incluyen indicadores como salud mental, tasa de desempleo, clase social, alcoholismo y suicidios.
- Este proceso se lleva a cabo en la **Capa Bronze**: Almacena los datos en bruto (JSON) para auditorías y reprocesos.

### Transformación

- **Capa Silver**: Datos procesados y estructurados en formato DataFrame, incluyendo eliminación de duplicados, manejo de valores nulos y estandarización.
- **Capa Gold**: Datos listos para análisis avanzado, con métricas calculadas como:
  - Índice de vulnerabilidad (desempleo, suicidios, alcoholismo, reingresos psiquiátricos).
  - Proporción de riesgo mental entre géneros.
  - Variabilidad de indicadores clave por comunidad autónoma.

### Carga y Visualización
- Los datos transformados son integrados en Power BI para visualizaciones interactivas, incluyendo:
  - Mapas geográficos.
  - Gráficos de tendencias temporales.
  - KPIs dinámicos.

## Resultados

Se llevó a cabo un análisis proactivo a partir de los gráficos y KPIs obtenidos, en el que se analizaron, entre otros, la tendencia anual de parámetros y la segmentación de género de los factores de riesgo.



## Conclusiones

El proyecto demuestra la eficacia de Microsoft Fabric y herramientas relacionadas en el manejo de datos complejos y la generación de insights accionables. La combinación de técnicas de análisis, almacenamiento y visualización proporciona un flujo de trabajo robusto y escalable, ideal para abordar problemáticas sociales y de salud.

## Cómo Ejecutar

1. **Requisitos**:
   - Acceso a Microsoft Fabric y Power BI.
   - Conexión a la API del Ministerio de Salud (requiere solicitud de token).

2. **Pasos**:
   - Cargar los datos en la capa Bronze mediante un notebook en Microsoft Fabric.
   - Realizar transformaciones en la capa Silver.
   - Procesar métricas avanzadas en la capa Gold.
   - Conectar Power BI al Lakehouse para crear visualizaciones.

## Autores

- **Marcos Tendero Carmona**
- **Néstor Álvarez Valencia**
- **Karen Lenis Arias**
- **Pablo Rodríguez Ramos**

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

---

Si necesitas alguna modificación o una sección adicional, ¡házmelo saber! 😊
