# Predicción de Riesgo de Obesidad mediante MLOps

# Descripción del Proyecto
Este proyecto implementa una solución End-to-End de Machine Learning y MLOps para la estimación del riesgo de obesidad a partir de hábitos alimenticios, actividad física y factores sociodemográficos.
La solución incorpora todo el ciclo de vida de un modelo de Machine Learning:
•	Análisis Exploratorio de Datos (EDA)
•	Ingeniería de características (Feature Engineering)
•	Entrenamiento y evaluación de modelos
•	Seguimiento de experimentos con MLflow
•	Orquestación de procesos mediante Prefect
•	Despliegue mediante FastAPI
•	Containerización con Docker
•	Estrategia de monitoreo
•	Testing y buenas prácticas

# Objetivo
Desarrollar una solución reproducible basada en MLOps que permita identificar individuos con riesgo de obesidad utilizando información relacionada con hábitos alimenticios, actividad física y antecedentes familiares.
La predicción se plantea como un problema de clasificación binaria:
•	1: Presenta riesgo de obesidad.
•	0: No presenta riesgo de obesidad.

# Dataset
El conjunto de datos utilizado corresponde al Obesity Dataset del repositorio UCI Machine Learning Repository (Dataset ID: 544).

# Características
•	2111 registros.
•	17 variables originales.
•	Información de individuos de México, Perú y Colombia.
•	Variables relacionadas con: 
o	Alimentación.
o	Actividad física.
o	Hábitos de vida.
o	Factores familiares.
•	Variable objetivo original: 
o	NObeyesdad (7 categorías).

# Variable objetivo del proyecto
La variable original fue transformada a una clasificación binaria:
Plain Text
1 = Riesgo de obesidad
0 = Sin riesgo de obesidad

# Arquitectura del Proyecto

Datos
|── Ingesta
|
|── EDA
|
|── Feature Engineering
|
|── Train/Test Split
|
|── Modelos ML
  |── Regresión Logística
  |── Random Forest
|── MLflow
|
|── Prefect
|
|── FastAPI
|
|── Docker
|
|── Monitoreo

# Tecnologías Utilizadas
## Ciencia de Datos
•	Python
•	Pandas
•	NumPy
•	Scikit-Learn
•	SciPy
## Visualización
•	Matplotlib
•	Seaborn
## MLOps
•	MLflow
•	Prefect
•	FastAPI
•	Docker
## Testing
•	Pytest
## Control de Versiones
•	Git
•	GitHub

# Modelos Implementados
## Regresión Logística
Utilizada como modelo baseline por su interpretabilidad y robustez para problemas de clasificación binaria.
## Random Forest
Utilizado para comparar desempeño frente al modelo baseline.

# Métricas de Evaluación
Los modelos son evaluados mediante:

## Accuracy
Porcentaje de clasificaciones correctas.
## Precision
Capacidad del modelo para evitar falsos positivos.
## Recall
Capacidad del modelo para detectar individuos con riesgo de obesidad.
## F1-Score
Balance entre Precision y Recall.
## ROC-AUC
Métrica principal utilizada para seleccionar el mejor modelo.

# Seguimiento de Experimentos con MLflow
MLflow se utiliza para:

•	Registrar parámetros.
•	Registrar métricas.
•	Comparar modelos.
•	Almacenar artefactos.
•	Seleccionar el mejor modelo.

# Orquestación con Prefect
Se implementó un flujo de trabajo utilizando Prefect para automatizar tareas del pipeline de entrenamiento.

# API de Predicción
El modelo es expuesto mediante FastAPI.
