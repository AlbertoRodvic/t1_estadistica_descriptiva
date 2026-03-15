# Trabajo 1 - Estadística Descriptiva Meteorológica

![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?logo=scipy&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Análisis exploratorio y estadística descriptiva de series meteorológicas diarias (2014-2025) en 10 celdas espaciales, organizado por apartados del enunciado y ejecutado en notebooks de Jupyter.

## Resumen Del Proyecto

- Variables analizadas: temperatura a 2 m, irradiación solar descendente en superficie y precipitación total.
- Cobertura temporal: 2014-01-01 a 2025-12-31.
- Resolución temporal: diaria (4383 filas por variable).
- Cobertura espacial: 10 celdas (01-10).
- Material generado: 38 figuras en la carpeta `images`.
- Flujo de trabajo: carga de datos, análisis por apartados, gráficas finales e informe.

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
|   `-- Gráficos exportados (1.x, 2.x, 3.x, 4.x y 7.x)
|-- documentation/
|   |-- Informe del trabajo.docx
|   |-- Informe del trabajo.pdf
|   |-- OBJETIVOS2026_TrabajoEstadisticaDescriptiva.pdf
|   |-- Plantilla_informe_trabajo_PRyES_2026.docx
|   `-- Trabajo1_2026_PRyES.pdf
|-- chu_DESCRIPTIVA_PRyES_v4.2.ipynb
|-- requirements.txt
|-- LICENSE
`-- README.md
```

## Dataset

Los tres CSV comparten estructura homogénea:

- Columna temporal: `FECHA`.
- 10 columnas de medida por celda (sufijo `CELDA01` a `CELDA10`).
- Columnas de calendario derivadas: `DIASEM`, `DIA`, `MES`, `ANNO`.

### Ficheros

- `G09B_2m_temperature.csv`: `TEMP_CELDA01` ... `TEMP_CELDA10`
- `G09B_surface_solar_radiation_downwards.csv`: `IRRAD_CELDA01` ... `IRRAD_CELDA10`
- `G09B_total_precipitation.csv`: `PRECIP_CELDA01` ... `PRECIP_CELDA10`

## Contenido Analítico (Por Apartados)

### Apartado 1

- Distribución de temperatura, irradiación y precipitación en celdas 01 y 10.
- Evolución por día de la semana, mes y año.
- Comparativa de variabilidad mensual y anual con coeficiente de variación.
- Gráficos generados: `Gráfico 1.1` a `Gráfico 1.16`.

### Apartado 2

- Relación entre temperatura de celdas 01 y 10.
- Matrices de correlación y pairplots para temperatura, irradiación y precipitación en las 10 celdas.
- Relación conjunta entre temperatura, irradiación y precipitación en la celda 01.
- Gráficos generados: `Gráfico 2.1`, `2.2`, `2.3` y `7.1` a `7.8`.

### Apartado 3

- Perfil mensual medio y mediano de temperatura e irradiación (celda 01).
- Evolución mensual de deciles (p10-p90) para temperatura e irradiación.
- Evolución anual de deciles de precipitación, incluyendo escala logarítmica.
- Identificación de años más secos y más húmedos según perfil mediano.
- Gráficos generados: `Gráfico 3.1` a `Gráfico 3.6`.

### Apartado 4

- Segmentación de celdas en dos grupos (01-05 y 06-10) basada en correlaciones.
- Series temporales de temperatura media y varianza por grupo.
- Correlación mensual entre medias y entre varianzas de ambos grupos.
- Gráficos generados: `Gráfico 4.1` a `Gráfico 4.4` y matriz complementaria `Gráfico 7.9`.

## Entorno Y Dependencias

Dependencias principales:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scipy`
- `jupyter` / `notebook` / `ipykernel`

Instalación recomendada:

```bash
python -m venv .venv
```

### Windows (PowerShell)

```bash
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### Linux / macOS

```bash
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Ejecución Reproducible

Orden sugerido para reproducir los resultados:

1. `src/carga_de_datos.ipynb` o carga desde `src/carga_de_datos.py`
2. `src/Apartado_1.ipynb`
3. `src/Apartado_2.ipynb`
4. `src/Apartado_3.ipynb`
5. `src/Apartado_4.ipynb`

Para lanzar Jupyter:

```bash
python -m notebook
```

## Convenciones Del Proyecto

- Los notebooks exportan figuras en alta calidad con `dpi=300` y `bbox_inches='tight'`.
- Los nombres de imagen siguen formato descriptivo (`Gráfico X.Y： ...`).
- Los apartados en `src` mantienen separación por objetivo analítico.
- El script de carga centraliza lectura y parseo de fechas para las 3 magnitudes.

## Documentación Entregable

En `documentation` se incluye:

- Enunciado y objetivos del trabajo.
- Plantilla de informe.
- Informe final en formato DOCX y PDF.

## Licencia

Proyecto bajo licencia MIT. Consulta el fichero `LICENSE` para el texto completo.
