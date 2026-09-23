# GEMMA × ReDLat — tutorial de exposoma

Tutorial para leer y trabajar con los datos de exposoma que **GEMMA**
(*Global Exposome Modeling, Mapping & Analytics*, la plataforma de BrainLat)
entrega a colaboradores de **ReDLat** (*The Multi-Partner Consortium to
Expand Dementia Research in Latin America*).

## Contenido

- **[`gemma_redlat_tutorial.ipynb`](gemma_redlat_tutorial.ipynb)** — el
  tutorial completo: qué es GEMMA y su relación con ReDLat, cómo está
  organizado el archivo de salida (`point_exposome_wide.csv`), qué
  significa cada radio de búsqueda (0/300/500/1000 m), y un tutorial
  práctico con pandas (cargar, filtrar, comparar, ancho↔largo). GitHub lo
  renderiza directo en el navegador — no hace falta clonar el repositorio ni
  tener Jupyter instalado.

## Por qué este notebook y no el pipeline completo

Este repositorio es deliberadamente acotado: el notebook es **100%
autocontenido** (solo `pandas`/`numpy`/`matplotlib`, sin ninguna
dependencia del código interno de GEMMA) y todos sus ejemplos se ejecutan
sobre un DataFrame **sintético** (participantes `EJ001`/`EJ002`/`EJ003`,
ficticios) — nunca sobre datos reales de participantes.

El pipeline de GEMMA (geocodificación, extracción de exposoma, la cohorte en
sí) es privado y vive en otro repositorio de BrainLat. Este tutorial es lo
único pensado para circular libremente entre colaboradores de ReDLat, y se
reutiliza cada vez que BrainLat entrega una descarga nueva.

## Cómo usarlo

1. Abrir [`gemma_redlat_tutorial.ipynb`](gemma_redlat_tutorial.ipynb) en
   GitHub para leerlo directo, o clonar el repositorio y abrirlo en
   Jupyter/VS Code para ejecutar las celdas (requiere Python 3.10+ con
   `pandas`, `numpy`, `matplotlib`).
2. Al recibir el archivo `point_exposome_wide.csv` correspondiente,
   sustituir el DataFrame de ejemplo (`example_wide`) por
   `pd.read_csv("point_exposome_wide.csv", dtype={"record_id": str})` y
   continuar con los mismos pasos sobre los datos reales.

## Contacto

Para solicitar una entrega nueva o una actualización, contactar al equipo
de BrainLat/GEMMA correspondiente.
