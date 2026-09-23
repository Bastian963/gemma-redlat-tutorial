# GEMMA × ReDLat — tutorial de exposoma

Tutorial para leer y trabajar con los datos de exposoma que **GEMMA**
(*Global Exposome Modeling, Mapping & Analytics*, la plataforma de BrainLat)
entrega a colaboradores de **ReDLat** (*The Multi-Partner Consortium to
Expand Dementia Research in Latin America*).

## Qué hay acá

- **[`gemma_redlat_tutorial.ipynb`](gemma_redlat_tutorial.ipynb)** — el
  tutorial completo: qué es GEMMA y su relación con ReDLat, cómo está
  organizado el CSV que te entregan (`point_exposome_wide.csv`), qué
  significa cada radio de búsqueda (0/300/500/1000 m), y un tutorial
  práctico con pandas (cargar, filtrar, comparar, ancho↔largo). GitHub lo
  renderiza directo en el navegador — no hace falta clonar nada ni tener
  Jupyter instalado, con solo abrir el link de arriba.
- **`assets/gemma_demo_worldmap.png`** — captura del explorador interactivo
  de GEMMA (mapa mundi pixel-art, click para entrar a cada ciudad).

## Por qué este notebook y no el pipeline completo

Este repositorio es deliberadamente chico: el notebook es **100%
autocontenido** (solo `pandas`/`numpy`/`matplotlib`, sin ninguna
dependencia del código interno de GEMMA) y todos sus ejemplos corren sobre
un DataFrame **sintético** (participantes `EJ001`/`EJ002`/`EJ003`,
inventados) — nunca sobre datos reales de participantes.

El pipeline de GEMMA (geocodificación, extracción de exposoma, la cohorte en
sí) es privado y vive en otro repositorio de BrainLat. Este tutorial es lo
único pensado para circular libremente entre colaboradores de ReDLat, y se
reutiliza cada vez que BrainLat entrega una descarga nueva.

## Cómo usarlo

1. Abrí [`gemma_redlat_tutorial.ipynb`](gemma_redlat_tutorial.ipynb) acá en
   GitHub para leerlo directo, o cloná el repo y abrilo en Jupyter/VS Code
   si preferís correr las celdas vos mismo (necesita Python 3.10+ con
   `pandas`, `numpy`, `matplotlib`).
2. Cuando tengas tu propio `point_exposome_wide.csv`, reemplazá el
   DataFrame de ejemplo (`example_wide`) por
   `pd.read_csv("point_exposome_wide.csv", dtype={"record_id": str})` y
   segui los mismos pasos con tus datos reales.

## Contacto

Para pedir una entrega nueva o una actualización, escribile al equipo de
BrainLat/GEMMA que te compartió tus datos.
