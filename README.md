# Estadistica Descriptiva Meteorologica

Proyecto de analisis exploratorio y descriptivo sobre series diarias de:
- temperatura
- irradiacion solar descendente en superficie
- precipitacion total

Los datos cubren 10 celdas espaciales y se trabajan en notebooks de Jupyter organizados por apartados del enunciado.

## Qué Encontraras En Este Repo

- Análisis univariante y comparativo entre celdas.
- Correlaciones entre celdas y entre variables meteorológicas.
- Perfiles mensuales (media, mediana y deciles).
- Perfil anual de precipitacion con visualizacion en escala lineal y logarítmica.
- Flujo reproducible desde carga de datos hasta gráficas finales.

## Estructura Del Proyecto

```text
.
|-- data/
|   |-- G09B_2m_temperature.csv
|   |-- G09B_surface_solar_radiation_downwards.csv
|   `-- G09B_total_precipitation.csv
|-- src/
|   |-- carga_de_datos.py
|   |-- carga_de_datos.ipynb
|   |-- Apartado_1.ipynb
|   |-- Apartado_2.ipynb
|   `-- Apartado_3.ipynb
|-- documentation/
|-- requirements.txt
|-- LICENSE
`-- README.md
```

## Stack Tecnológico

- Python 3.10+
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- seaborn
- scipy

## Instalación Rápida

```bash
python -m pip install -r requirements.txt
```

Si no tienes Jupyter instalado globalmente, puedes iniciarlo con:

```bash
python -m notebook
```

## Orden Recomendado De Ejecución

1. `src/carga_de_datos.ipynb`
2. `src/Apartado_1.ipynb`
3. `src/Apartado_2.ipynb`
4. `src/Apartado_3.ipynb`

## Resultados Que Se Analizan

- Diferencias entre perfil medio y mediano por mes.
- Meses (o anos) con mínimos y máximos segun perfil mediano.
- Apertura entre deciles para estudiar variabilidad.
- Cambios de dispersión temporal en temperatura, irradiación y precipitación.

## Convenciones Del Proyecto

- Archivos de apartados con `snake_case` y guion bajo: `Apartado_1.ipynb`, etc.
- Variables con sufijos por magnitud para evitar ambigüedad:
	- `_temp` para temperatura
	- `_irrad` para irradiación
	- `_precip` para precipitación

## Licencia

Este proyecto se distribuye bajo licencia MIT. Consulta `LICENSE` para mas detalles.
