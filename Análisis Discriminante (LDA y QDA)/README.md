# Comparacion de LDA y QDA sobre el dataset Wine

Implementacion y comparacion del Analisis Discriminante
Lineal (LDA) y el Analisis Discriminante Cuadratico (QDA) utilizando el
conjunto de datos Wine, sin tratamiento previo.

## Contenido del repositorio

```
.
├── LDA_QDA_Wine.ipynb   # Notebook completo con el analisis y los modelos
└── README.md
```

## Como obtener el conjunto de datos

El dataset **no requiere descarga manual**, ya que se carga directamente
dentro del notebook mediante scikit-learn:

```python
from sklearn.datasets import load_wine
datos_wine = load_wine()
```

Esto descarga el dataset Wine (UCI Machine Learning Repository) de forma
automatica al ejecutar la celda correspondiente, garantizando que se use
sin ningun tratamiento o modificacion previa, tal como lo exige la consigna
del proyecto.

- **Fuente original:** UCI Machine Learning Repository
- **Numero de observaciones:** 178
- **Variables predictoras:** 13 (todas numericas, resultado de un analisis
  quimico de vinos)
- **Variable objetivo:** cultivar (3 clases)

## Como ejecutar el proyecto

1. Abrir el archivo `LDA_QDA_Wine.ipynb` en Google Colab (o Jupyter Notebook
   local).
2. Ejecutar las celdas en orden, de arriba hacia abajo (`Entorno de
   ejecucion → Ejecutar todas` en Colab).
3. No se requiere subir ningun archivo adicional, ya que el dataset se
   carga automaticamente desde scikit-learn en la primera celda de codigo.

### Librerias utilizadas

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

Todas estan preinstaladas por defecto en Google Colab.

## Estructura del notebook

1. Descripcion del conjunto de datos
2. Exploracion de los datos (dimensiones, tipos, valores faltantes,
   estadisticas descriptivas, distribucion de clases)
3. Visualizacion (histograma, dispersion, mapa de correlaciones, boxplot)
4. Preparacion de los datos (train/test split, estandarizacion)
5. Implementacion de LDA (entrenamiento, matriz de confusion, metricas)
6. Implementacion de QDA (entrenamiento, matriz de confusion, metricas)
7. Comparacion de modelos (metricas, tiempo de entrenamiento)
8. Fronteras de decision (visualizacion 2D de LDA vs QDA)
9. Conclusiones

## Principales hallazgos

- Tanto LDA como QDA obtienen un desempeno alto sobre el dataset Wine, con
  metricas de accuracy, precision, recall y F1-Score cercanas entre si.
- Las variables **flavonoides** y **prolina** muestran una separacion visual
  clara entre las tres clases, siendo buenas candidatas para representar
  las fronteras de decision en 2D.
- La frontera de decision de LDA es lineal (regiones poligonales), mientras
  que la de QDA es curva, como consecuencia directa de que QDA estima una
  matriz de covarianza distinta por cada clase.
- Dado el desempeno similar entre ambos modelos en este dataset, se
  recomienda LDA por su menor complejidad y mayor estabilidad con un
  tamano de muestra reducido (178 observaciones).

## Autora

Scarlett - Universidad de Guayaquil, Ciencia de Datos e Inteligencia
Artificial.
