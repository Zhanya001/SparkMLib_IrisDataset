# Clasificación del Iris Dataset usando Spark MLlib

Este proyecto realiza la predicción del Iris Dataset utilizando tres algoritmos de clasificación diferentes implementados con Spark MLlib:

- **Decision Tree Classifier**
- **Gradient-Boosted Tree Classifier**
- **Random Forest Classifier**

## Objetivos

- **Transformar en vector los datos numéricos** usando `VectorAssembler`.
- **Transformar los datos de la columna especies** usando `StringIndexer`.
- **Calcular la predicción y la precisión del modelo** empleando:
  - `DecisionTreeClassifier`
  - `GBTClassifier`
  - `RandomForestClassifier`

## Descripción

El objetivo es entrenar y evaluar modelos de clasificación para predecir la especie de las flores de iris basándose en sus características morfológicas. Debido a limitaciones del `GBTClassifier` en algunas versiones de Spark, se realiza una **clasificación binaria** utilizando solo dos de las tres especies disponibles en el dataset.

## Requisitos

- **Python** 3.7 o superior
- **Apache Spark** 3.0 o superior
- **Java JDK** 8 o superior

## Instalación

1. **Clonar el repositorio**:

   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
   ```

2. **Crear un entorno virtual (opcional pero recomendado)**:
   
   ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows: venv\Scripts\activate
    ```

3. **Instalar las dependencias**:

    ```bash
    pip install -r requirements.txt
    ```

# Resultados Esperados
Al ejecutar el script, deberías obtener una salida similar a:

```bash
+-----------------+----------------+-----------------+----------------+-------+
|sepal length (cm)|sepal width (cm)|petal length (cm)|petal width (cm)|species|
+-----------------+----------------+-----------------+----------------+-------+
|              5.1|             3.5|              1.4|             0.2|      0|
|              4.9|             3.0|              1.4|             0.2|      0|
|              4.7|             3.2|              1.3|             0.2|      0|
|              4.6|             3.1|              1.5|             0.2|      0|
|              5.0|             3.6|              1.4|             0.2|      0|
+-----------------+----------------+-----------------+----------------+-------+
only showing top 5 rows

+-------+-----+-----------------+
|species|label|         features|
+-------+-----+-----------------+
|      0|  1.0|[5.1,3.5,1.4,0.2]|
|      0|  1.0|[4.9,3.0,1.4,0.2]|
|      0|  1.0|[4.7,3.2,1.3,0.2]|
|      0|  1.0|[4.6,3.1,1.5,0.2]|
|      0|  1.0|[5.0,3.6,1.4,0.2]|
+-------+-----+-----------------+
only showing top 5 rows

+-----+-----+
|label|count|
+-----+-----+
|  0.0|   39|
|  1.0|   41|
+-----+-----+

Precisión del modelo Decision Tree: 1.0000
Precisión del modelo Gradient-Boosted Tree: 1.0000
Precisión del modelo Random Forest: 1.0000
```

### Notas
- Clasificación Binaria: Debido a limitaciones del GBTClassifier, el dataset se ha filtrado para incluir solo dos especies, permitiendo así la clasificación binaria.
- Compatibilidad: Asegúrate de que las versiones de Spark y Java en tu sistema son compatibles.

## Obtención del Dataset (fuente)

Puedes descargar el dataset `iris.csv` desde el repositorio de [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/iris) y colocarlo en la raíz del proyecto.


## Contacto
Si tienes preguntas o deseas más información, puedes contactarme a través de [LinkedIn: Ariet Michal](https://www.linkedin.com/in/ariet-michal)