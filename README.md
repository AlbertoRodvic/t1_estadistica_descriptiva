<div align="center">

# Trabajo 1 - Estadística Descriptiva Meteorológica

Análisis exploratorio de series meteorológicas diarias (2014-2025) en 10 celdas espaciales, construido en Jupyter con foco en trazabilidad, reproducibilidad y calidad del informe final.

![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?logo=scipy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

</div>

---

## Qué Incluye Este Repositorio

- Pipeline de carga unificado para temperatura, irradiación y precipitación.
- Desarrollo analítico dividido por apartados (`Apartado_1` a `Apartado_4`).
- Exportación de figuras y documentación final del trabajo.
- Estructura preparada para colaboración y revisiones por PR.

## Snapshot Del Proyecto

| Aspecto | Detalle |
|---|---|
| Dominio | Estadística descriptiva meteorológica |
| Cobertura temporal | 2014-01-01 a 2025-12-31 |
| Frecuencia | Diaria |
| Número de observaciones | 4383 filas por variable |
| Cobertura espacial | 10 celdas (CELDA01-CELDA10) |
| Variables principales | Temperatura 2m, irradiación solar descendente, precipitación total |
| Salidas | Notebooks + figuras + informe en DOCX/PDF |

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
|-- documentation/
|-- CONTRIBUTING.md
|-- CODE_OF_CONDUCT.md
|-- SECURITY.md
|-- requirements.txt
|-- LICENSE
|-- .gitignore
`-- README.md
```

## Puesta En Marcha Rápida

1. Crear entorno virtual:

```bash
python -m venv .venv
```

2. Activar entorno:

Windows (PowerShell):

```bash
.\.venv\Scripts\Activate.ps1
```

Linux / macOS:

```bash
source .venv/bin/activate
```

3. Instalar dependencias:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

4. Iniciar entorno de notebooks:

```bash
python -m notebook
```

## Orden De Ejecución Recomendado

Para reconstruir resultados de forma consistente:

1. `src/carga_de_datos.ipynb` (o `src/carga_de_datos.py`)
2. `src/Apartado_1.ipynb`
3. `src/Apartado_2.ipynb`
4. `src/Apartado_3.ipynb`
5. `src/Apartado_4.ipynb`

## Datos

Todos los CSV comparten esquema común:

- Columna temporal: `FECHA`
- Variables por celda: `CELDA01` a `CELDA10`
- Variables calendario derivadas: `DIASEM`, `DIA`, `MES`, `ANNO`

| Archivo | Variables | Descripción |
|---|---|---|
| `G09B_2m_temperature.csv` | `TEMP_CELDAxx` | Temperatura a 2 metros |
| `G09B_surface_solar_radiation_downwards.csv` | `IRRAD_CELDAxx` | Irradiación solar descendente |
| `G09B_total_precipitation.csv` | `PRECIP_CELDAxx` | Precipitación total |

## Ruta Analítica

| Apartado | Objetivo |
|---|---|
| 1 | Caracterización univariante y temporal (celdas 01 y 10) |
| 2 | Dependencias bivariantes/multivariantes y relaciones estructurales |
| 3 | Perfiles temporales, deciles y comparación de años secos/húmedos |
| 4 | Segmentación de celdas y comparación por grupos |

## Colaboración

Este repositorio incorpora archivos de colaboración estándar:

- Guía de contribución en `CONTRIBUTING.md`
- Código de conducta en `CODE_OF_CONDUCT.md`
- Política de seguridad en `SECURITY.md`
- Plantillas de issues y PR en `.github/`

## Licencia

Proyecto distribuido bajo licencia MIT. Consulta `LICENSE` para el texto completo.
