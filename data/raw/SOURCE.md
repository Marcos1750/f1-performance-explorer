# Fuente de los datos crudos

Los seis CSV provienen del repositorio público [TracingInsights/RaceData](https://github.com/TracingInsights/RaceData), que documenta estos archivos como una copia actualizada del dataset relacional de Fórmula 1 publicado en Kaggle y derivado originalmente de Ergast/Jolpica.

- Commit fijado: `57febd417e981e17d3d43680727abc6a2f46e03d`
- Descarga realizada: 2026-09-10
- Carpeta de origen: `data/`
- Licencia declarada por el repositorio: CC0 (dominio público)
- Documentación del esquema: https://github.com/TracingInsights/RaceData/blob/main/F1_data_folder_documentation.md

## Archivos elegidos

| Archivo | Motivo |
|---|---|
| `races.csv` | temporada, ronda, fecha, nombre y clave del circuito |
| `results.csv` | resultado de cada piloto por carrera |
| `drivers.csv` | nombres y datos descriptivos de pilotos |
| `constructors.csv` | nombres y datos descriptivos de escuderías |
| `circuits.csv` | traduce `circuitId` a un circuito legible |
| `status.csv` | traduce `statusId` al estado final legible |

Los archivos contienen todas las temporadas disponibles. El filtro de 2019 se hará dentro del notebook, de forma visible y reproducible. No modifiques estos CSV; cualquier tabla derivada debe guardarse en `data/processed/`.

## Integridad SHA-256

```text
a43c986bf3f4b3856682e0f8d14bb2c07fab578ce670421c6b96507c151c9590  circuits.csv
a80601ac9f6961221527682452aa99c3075e8bddf5bb12e1eca95052aee52600  constructors.csv
d0a061348fc6874762691c0839db0a55102d3b5120d0f0cb39e74cd4635308f8  drivers.csv
cfe8bb2f79b62abe3af108473c963a4600fd71e3861ee1f9489d489a45d5064d  races.csv
615adc550c503fa63b9671cea66c72ba0c6c1a08bd8d14b32f7e6ceedd9ea6b3  results.csv
6651b8a26b6efd60fde9f7d6a2dd8523c80910918c5e9fe97a9c3136ef5fba2d  status.csv
```

