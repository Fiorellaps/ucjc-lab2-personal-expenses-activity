<img src="https://iddigitalschool.com/wp-content/uploads/2024/03/UCJC-Horizontal_Granate.png" alt="Universidad Camilo José Cela" width="300">

# Laboratorio 2 · Gastos personales

Programación Avanzada y Entornos de Desarrollo para la IA · Tema 2

Análisis de un conjunto de datos de gastos personales de 10 000 personas: revisarás su calidad, lo limpiarás, buscarás patrones, lo prepararás para entrenar un modelo y presentarás los resultados en un dashboard con Shiny. Pondrás en práctica lo visto en el Tema 2: calidad y limpieza de datos, transformación de variables, análisis exploratorio, visualización y preparación para modelado.

## Qué vas a practicar

| Paso | Contenido |
|---|---|
| Entorno y dependencias | `venv` o `uv`, `requirements.txt` (como en el Laboratorio 1) |
| Carga y primer vistazo | estructura, tipos y estadísticos básicos |
| Diagnóstico de calidad | nulos, duplicados, categorías, rangos, coherencia entre columnas, atípicos |
| Limpieza y transformación | tipos categóricos y booleanos, variables derivadas, marcas de calidad |
| Análisis exploratorio | distribuciones, correlaciones y comparación por grupos |
| Preparación para modelado | codificación, escalado y partición train/test sin fuga de información |
| Git, GitHub y uso de IA | repositorio, commits claros, README y reflexión sobre el asistente de programación |

## Archivos

| Archivo | Contenido |
|---|---|
| `src/lab2_gastos_personales.ipynb` | Notebook que tienes que completar |
| `data/raw/personal_spending_dataset.csv` | Datos del laboratorio |
| `requirements.txt` | Librerías usadas en la solución, con las versiones probadas |
| `Laboratorio2_enunciado.docx` | Enunciado de la actividad |

## Cómo empezar

```bash
python -m venv .venv
source .venv/bin/activate        # en Windows: .venv\Scripts\activate
pip install -r requirements.txt jupyterlab
jupyter lab src/lab2_gastos_personales.ipynb
```

## Dashboard de ejemplo

`src/app_shiny.py` es un dashboard de Shiny for Python que lee `data/processed/gastos_limpio.csv`, generado al ejecutar el notebook resuelto. Tiene filtros por ocupación, zona y edad, y permite excluir las filas con problemas de calidad.

```bash
shiny run src/app_shiny.py       # abre http://127.0.0.1:8000
```
