# Reconocimiento de Dígitos con Aprendizaje Supervisado: MNIST, k-NN y Regresión Logística

Este repositorio presenta un proyecto de machine learning supervisado orientado al reconocimiento de dígitos manuscritos utilizando el conjunto de datos MNIST. Se desarrollan y comparan dos modelos de clasificación: k-Nearest Neighbors (k-NN) y regresión logística.

## Datos utilizados

- `MNIST.csv`: versión reducida del conjunto MNIST con imágenes de 28x28 píxeles representadas como vectores de 784 características.
- `numero.jpg`: imagen personalizada de un dígito creada por el usuario para realizar una predicción práctica con los modelos entrenados.

## Etapas del proyecto

### 1. Carga y visualización de datos
- Se cargan los datos con `pandas` y se imprime una imagen como matriz de 28x28 usando `matplotlib`.

### 2. Modelado con k-NN
- División de datos en entrenamiento (70%) y prueba (30%) con `train_test_split`
- Entrenamiento del modelo con `KNeighborsClassifier(n_neighbors=14)`
- Evaluación con `accuracy_score()`
- Predicción personalizada sobre imagen externa convertida a vector compatible

### 3. Regresión Logística
- Entrenamiento con `LogisticRegression(solver="newton-cg")`
- Cálculo de precisión, pesos del modelo, e interpretación del intercepto
- Generación del `classification_report` por clase
- Aplicación sobre imagen externa y predicción visual

### 4. Análisis de Overfitting y selección de k
- Prueba de valores de `k` entre 1 y 8
- Visualización de precisión en entrenamiento y prueba para detectar sobreajuste o infraajuste

## Métricas de evaluación

- Precisión global (`accuracy`) para ambos modelos
- f1-score, recall y precision por clase en regresión logística
- AUC y curva ROC para evaluar la efectividad del modelo logístico

## Tecnologías utilizadas

- Python 3.x  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- PIL  

## Conclusión

- El modelo k-NN alcanza una precisión del 95.67% sobre MNIST, mientras que la regresión logística obtiene un 89.95%.
- La curva ROC y el classification report muestran la consistencia de ambos modelos por clase.
- La imagen personalizada fue clasificada correctamente, demostrando la aplicabilidad del modelo en datos externos.
