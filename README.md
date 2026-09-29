# F1 Performance Explorer

Análisis reproducible de la temporada 2019 de Fórmula 1 con NumPy, Pandas y Matplotlib.

## Pregunta central

¿Qué pilotos y escuderías rindieron mejor durante la temporada, y cuáles consiguieron resultados superiores o inferiores a su posición de largada?

## Alcance de la primera versión

- Temporada: **2019**.
- Unidad de análisis final: un piloto en un Gran Premio.
- Incluye únicamente resultados de los Grandes Premios.
- No incluye telemetría, vueltas, neumáticos, API, SQL, aplicaciones web ni modelos predictivos.
- Seaborn se incorporará después de validar las métricas y los primeros gráficos con Matplotlib.

Se eligió 2019 porque contiene 21 Grandes Premios, no tiene carreras sprint y evita que una exclusión inicial de sprints produzca una evolución de puntos incompleta. También es una temporada histórica cerrada y estable.

## Estructura

```text
f1-performance-explorer/
├── data/
│   ├── raw/          # CSV originales: no se editan
│   └── processed/    # salidas creadas por el notebook
├── figures/          # gráficos exportados
├── notebooks/
│   └── f1_performance_explorer.ipynb
├── README.md
└── requirements.txt
```

Los datos crudos y su versión exacta están documentados en `data/raw/SOURCE.md`.

## Puesta en marcha

Desde esta carpeta:

```powershell
py -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
.venv\Scripts\python -m jupyter lab
```

Abrí `notebooks/f1_performance_explorer.ipynb` y ejecutá las celdas en orden.

