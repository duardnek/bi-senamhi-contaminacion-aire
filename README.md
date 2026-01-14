# 🌍 BI-SENAMHI: Inteligencia de Negocios para el Monitoreo de Calidad del Aire y Salud en Lima

![Data Analysis](https://img.shields.io/badge/Focus-Business%20Intelligence-blue)
![SQL Server](https://img.shields.io/badge/DB-SQL%20Server-red)
![Power BI](https://img.shields.io/badge/Viz-Power%20BI-yellow)
![Status](https://img.shields.io/badge/Status-Completed-success)

Este proyecto desarrolla una solución integral de **Business Intelligence (BI)** para centralizar, analizar y visualizar datos sobre contaminantes atmosféricos (PM2.5, PM10, NO₂) y su correlación con Infecciones Respiratorias Agudas (IRA) en Lima Metropolitana, utilizando datos abiertos de **SENAMHI** y del sistema de vigilancia epidemiológica.

## 📊 Propósito del Proyecto
Transformar datos heterogéneos y dispersos en información estratégica que permita a las autoridades y ciudadanos identificar periodos críticos de contaminación y entender el impacto real de la calidad del aire en la salud pública de los distritos monitoreados.

## 🛠️ Stack Tecnológico
* **Base de Datos (OLTP):** Microsoft SQL Server.
* **ETL (Extracción, Transformación y Carga):** SQL Server Integration Services (SSIS).
* **Data Mart (OLAP):** Diseño en esquema de estrella (Star Schema).
* **Visualización de Datos:** Power BI Desktop / Power BI Service.
* **Lenguajes:** T-SQL (Scripts de BD) y DAX (Medidas analíticas).

## 🏗️ Arquitectura de la Solución
El sistema sigue el flujo clásico de una solución de BI:
1.  **Fuentes de Datos:** Datasets de SENAMHI (Contaminación) y registros de salud (IRAs, Neumonías, Defunciones).
2.  **Staging & ETL:** Limpieza de datos, manejo de nulos y estandarización de unidades de medida.
3.  **Data Mart (DMSenamhi):** * **Hechos:** `THContaminacion` y `Fact_AireSalud`.
    * **Dimensiones:** `DimEstacion`, `DimUbicacion`, `DimTiempo`, `DimContaminante`.



## 📈 Dashboards Principales
El reporte de Power BI incluye 5 páginas de análisis profundo:
* **Resumen General:** KPI's de niveles de contaminación actuales.
* **Análisis Temporal:** Evolución histórica por mes y año.
* **Comparativa de Estaciones:** Identificación de las zonas con mayor carga contaminante.
* **Alertas de Calidad:** Comparación contra los Estándares de Calidad Ambiental (ECA).
* **Correlación Aire-Salud:** Cruce de datos entre niveles de PM2.5/PM10 y el incremento de enfermedades respiratorias por grupo etario.



## 🚀 Cómo empezar
1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/nombre-del-repo.git](https://github.com/tu-usuario/nombre-del-repo.git)
    ```
2.  **Base de Datos:** Ejecuta los scripts de la carpeta `/sql` para crear la estructura de tablas.
3.  **Procesos ETL:** Abre el proyecto de SSIS en Visual Studio para cargar los datos desde los archivos fuente en `/data`.
4.  **Power BI:** Abre el archivo `.pbix` y configura la cadena de conexión a tu servidor local.

## 👥 Autores
Proyecto desarrollado por estudiantes de Ingeniería de Sistemas de la **Universidad César Vallejo**:
* **Cavero Gomero, Sandro Luis**
* **Castro Quicaña, Eduardo Franco**
* **Cruz Laos, Piero Fabrizio**
* **Diaz Asto, Franz Jhamir**
* **Gonzales Lopez, Benjamin Elivelton**
* **Soto Romero, Jack Steven Francesco**

**Asesor:** Dr. Flores Chacón, Erick Giovanny

## 📄 Licencia
Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo `LICENSE` para más detalles.
