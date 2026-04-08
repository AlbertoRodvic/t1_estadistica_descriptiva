<div align="center">

# Trabajo 1 - Estadistica Descriptiva Meteorologica

Analisis exploratorio completo de series meteorologicas diarias (2014-2025) en 10 celdas espaciales, desarrollado en Jupyter con enfoque reproducible y documentacion final en DOCX/PDF.

![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?logo=scipy&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

</div>

---

## Vision General

| Aspecto | Detalle |
|---|---|
| Dominio | Estadistica descriptiva meteorologica |
| Variables | Temperatura 2 m, irradiacion solar descendente, precipitacion total |
| Cobertura temporal | 2014-01-01 a 2025-12-31 |
| Resolucion | Diaria (4383 registros por variable) |
| Cobertura espacial | 10 celdas (CELDA01-CELDA10) |
| Salida grafica | 37 figuras exportadas en `images/` |
| Entregables | Notebooks, script de carga, informe final DOCX y PDF |

## Indice

- [Estructura Del Repositorio](#estructura-del-repositorio)
- [Dataset](#dataset)
- [Ruta Analitica](#ruta-analitica)
- [Puesta En Marcha](#puesta-en-marcha)
- [Ejecucion Reproducible](#ejecucion-reproducible)
- [Convenciones Del Proyecto](#convenciones-del-proyecto)
- [Documentacion Entregable](#documentacion-entregable)
- [Licencia](#licencia)

## Estructura Del Repositorio

```text
.
|-- src/
|   |-- carga_de_datos.py
|   |-- carga_de_datos.ipynb
|   |-- Apartado_1.ipynb
|   |-- Apartado_2.ipynb
|   |-- Apartado_3.ipynb
|   `-- Apartado_4.ipynb
|-- DATOS_IMAT_2026/
|   |-- G09B_2m_temperature.csv
|   |-- G09B_surface_solar_radiation_downwards.csv
|   `-- G09B_total_precipitation.csv
|-- images/
|   `-- Graficos exportados (1.x, 2.x, 3.x, 4.x y 7.x)
|-- documentation/
|   |-- Informe del trabajo.docx
|   |-- Informe del trabajo.pdf
|   |-- OBJETIVOS2026_TrabajoEstadisticaDescriptiva.pdf
|   |-- Plantilla_informe_trabajo_PRyES_2026.docx
|   `-- Trabajo1_2026_PRyES.pdf
|-- requirements.txt
|-- LICENSE
|-- .gitignore
`-- README.md
```

## Dataset

Los tres CSV tienen estructura homogenea y permiten analisis comparables por variable y por celda.

### Esquema Comun

- Columna temporal: `FECHA`
- Variables por celda: 10 columnas por magnitud (`CELDA01` a `CELDA10`)
- Columnas derivadas de calendario: `DIASEM`, `DIA`, `MES`, `ANNO`

### Ficheros

| Archivo | Prefijo De Variables | Descripcion |
|---|---|---|
| `G09B_2m_temperature.csv` | `TEMP_CELDAxx` | Temperatura a 2 metros |
| `G09B_surface_solar_radiation_downwards.csv` | `IRRAD_CELDAxx` | Irradiacion solar descendente |
| `G09B_total_precipitation.csv` | `PRECIP_CELDAxx` | Precipitacion total |

## Ruta Analitica

| Apartado | Objetivo Principal | Salida Grafica |
|---|---|---|
| 1 | Caracterizacion univariante y temporal de celdas 01 y 10 | Graficos 1.1-1.16 |
| 2 | Correlaciones y relaciones bivariantes/multivariantes | Graficos 2.1-2.3 y 7.1-7.8 |
| 3 | Perfiles mensuales, deciles y comparativas de anos secos/humedos | Graficos 3.1-3.6 |
| 4 | Segmentacion de celdas y comparacion entre grupos 01-05 vs 06-10 | Graficos 4.1-4.4 |

## Puesta En Marcha

### 1) Crear Entorno

```bash
python -m venv .venv
```

### 2) Activar Entorno

Windows (PowerShell):

```bash
.\.venv\Scripts\Activate.ps1
```

Linux / macOS:

```bash
source .venv/bin/activate
```

### 3) Instalar Dependencias

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Ejecucion Reproducible

Orden recomendado para reconstruir resultados y figuras:

1. `src/carga_de_datos.ipynb` (o alternativa script: `src/carga_de_datos.py`)
2. `src/Apartado_1.ipynb`
3. `src/Apartado_2.ipynb`
4. `src/Apartado_3.ipynb`
5. `src/Apartado_4.ipynb`

Para abrir el entorno de notebooks:

```bash
python -m notebook
```

## Convenciones Del Proyecto

- Exportacion de figuras con calidad alta (`dpi=300`, `bbox_inches='tight'`).
- Nombres de imagen descriptivos siguiendo el formato `Grafico X.Y: Titulo`.
- Separacion por objetivos analiticos en notebooks independientes.
- Carga y parseo de fechas centralizados para las tres magnitudes.

## Documentacion Entregable

En `documentation/` se incluye:

- Informe final en `DOCX` y `PDF`
- Plantilla del informe
- Enunciado y documento base de la asignatura

## Licencia

Este proyecto se distribuye bajo licencia MIT. Consulta `LICENSE` para el texto completo.
