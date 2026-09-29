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

## Continuar desde otra computadora

En la otra computadora, iniciá sesión en GitHub con la cuenta que tiene acceso al repositorio. Después, desde la carpeta donde quieras guardar el proyecto:

```powershell
git clone https://github.com/Marcos1750/f1-performance-explorer.git
cd f1-performance-explorer
py -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
.venv\Scripts\python -m jupyter lab
```

El entorno `.venv` se crea en cada computadora y no se sube a GitHub. Los CSV originales y el notebook sí están en el repositorio. Ejecutá el notebook desde el principio después de clonarlo para reconstruir las variables de Python.

Para llevar los cambios de una computadora a la otra, guardá el notebook y, en la primera, ejecutá:

```powershell
git status
git add notebooks/f1_performance_explorer.ipynb
git commit -m "Actualizar análisis"
git push
```

En la segunda, ejecutá `git pull` antes de seguir trabajando. Evitá editar el mismo notebook en ambas computadoras sin sincronizar entre medio.

