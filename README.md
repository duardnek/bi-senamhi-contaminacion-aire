# 🌍 BI-SENAMHI: Sistema de Inteligencia de Negocios para el Monitoreo de Calidad del Aire y Salud Pública

[![SQL Server](https://img.shields.io/badge/Database-SQL%20Server-red?style=flat-square&logo=microsoft-sql-server)](https://www.microsoft.com/sql-server)
[![SSIS](https://img.shields.io/badge/ETL-SSIS-orange?style=flat-square)](https://docs.microsoft.com/sql/integration-services/)
[![Power BI](https://img.shields.io/badge/Visualización-Power%20BI-yellow?style=flat-square&logo=power-bi)](https://powerbi.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](https://opensource.org/licenses/MIT)

## 📋 Descripción del Proyecto
Este proyecto desarrolla una solución de Business Intelligence (BI) extremo a extremo para el análisis de contaminantes atmosféricos (PM2.5, PM10, NO₂) en Lima Metropolitana. La innovación principal radica en la integración de datos abiertos del SENAMHI con indicadores epidemiológicos de Infecciones Respiratorias Agudas (IRA)**, permitiendo identificar correlaciones críticas entre la calidad del aire y la salud pública.

## 🚀 Desafío Técnico
* **Fragmentación de Datos:** Consolidación de fuentes heterogéneas (SENAMHI y Vigilancia Epidemiológica).
* **Calidad de Datos:** Tratamiento de valores nulos y estandarización de unidades de medida ambiental.
* **Escalabilidad:** Diseño de un modelo dimensional que soporte el crecimiento histórico de registros de monitoreo.

## 🛠️ Stack Tecnológico
* **Data Warehouse:** Microsoft SQL Server (OLTP y Data Mart).
* **Ingeniería de Datos (ETL):** SQL Server Integration Services (SSIS).
* **Modelado:** Star Schema (Esquema de Estrella) con dimensiones de Tiempo, Ubicación y Estación.
* **Analítica:** Power BI utilizando lenguaje DAX para métricas avanzadas y comparativas contra los ECAs (Estándares de Calidad Ambiental).

## 🏗️ Arquitectura de Datos
El sistema se basa en un **Data Mart (DMSenamhi)** estructurado de la siguiente manera:
- **Hechos:** - `THContaminacion`: Métricas horarias/diarias de contaminantes.
    - `Fact_AireSalud`: Tabla agregada que vincula promedios anuales de polución con tasas de mortalidad y hospitalización por IRA.
- **Dimensiones:** Estación, Contaminante, Tiempo (Jerárquico) y Ubicación Geográfica.

## 📊 Dashboards de Alto Impacto
Se diseñaron 5 vistas analíticas orientadas a la toma de decisiones:
1. **Vista Gerencial:** Indicadores clave (KPIs) de calidad del aire actual.
2. **Análisis de Tendencias:** Evolución histórica y estacionalidad de contaminantes.
3. **Benchmarking de Estaciones:** Ranking de los distritos con mayor estrés ambiental.
4. **Cumplimiento Normativo:** Semáforo de alertas basado en límites de la OMS y MINAM.
5. **Panel Aire-Salud:** Correlación visual entre niveles de NO₂/PM2.5 y el incremento de neumonías y defunciones.

## 👥 Equipo de Desarrollo
Proyecto realizado por estudiantes de Ingeniería de Sistemas - **Universidad César Vallejo**:
* **Sandro Cavero** | **Eduardo Castro** | **Piero Cruz**
* **Franz Diaz** | **Benjamin Gonzales** | **Jack Soto**

**Asesor:** Dr. Erick Giovanny Flores Chacón

---
*Este proyecto fue desarrollado bajo los estándares de los Objetivos de Desarrollo Sostenible (ODS), promoviendo ciudades y comunidades más sostenibles.*
