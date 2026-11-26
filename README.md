# Segmentación de clientes mediante K-Means y PCA en AWS EC2

## Descripción del proyecto

Esta práctica consiste en implementar un modelo de aprendizaje no supervisado para segmentar clientes de comercio electrónico mediante K-Means y reducción de dimensionalidad con PCA dentro de una instancia Ubuntu en AWS EC2.

## Objetivo

Identificar grupos de clientes con características similares, determinar el número óptimo de clusters mediante métricas de validación interna y reducir la dimensionalidad de los datos.

## Tecnologías utilizadas

- AWS Academy Learner Lab
- AWS EC2
- Ubuntu
- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib
- GitHub

## Metodología

1. Generación de un conjunto de 1,200 clientes simulados con seis características.
2. Estandarización de datos mediante StandardScaler.
3. Evaluación de K-Means con valores de K entre 2 y 5.
4. Comparación de las métricas Silhouette, Davies-Bouldin y Calinski-Harabasz.
5. Selección del número óptimo de clusters.
6. Entrenamiento del modelo final K-Means.
7. Reducción de dimensionalidad de seis a dos componentes mediante PCA.
8. Serialización de los tres artefactos generados.

## Archivos del proyecto

| Archivo | Descripción |
|---|---|
| practica_segmentacion_ec2.py | Código principal del proyecto. |
| modelo_kmeans_clientes.pkl | Modelo K-Means entrenado. |
| scaler_clientes.pkl | Escalador de características. |
| pca_clientes.pkl | Modelo de reducción de dimensionalidad. |
| resultados.txt | Métricas obtenidas durante la ejecución. |
| requirements.txt | Dependencias del proyecto. |

## Resultados obtenidos

| Métrica | Resultado |
|---|---|
| Número óptimo de clusters (K) | Pendiente |
| Coeficiente de Silueta | Pendiente |
| Índice Davies-Bouldin | Pendiente |
| Índice Calinski-Harabasz | Pendiente |
| Varianza explicada por PCA | Pendiente |

## Instalación y ejecución

Crear el entorno virtual:

`python3 -m venv venv`

Activar el entorno virtual:

`source venv/bin/activate`

Instalar las dependencias:

`pip install -r requirements.txt`

Ejecutar el programa:

`python3 practica_segmentacion_ec2.py`

## Integración en producción

El escalador permite transformar los datos de nuevos clientes utilizando la misma estandarización aplicada durante el entrenamiento.

El modelo K-Means utiliza los datos estandarizados para asignar a cada cliente un segmento.

PCA permite reducir los datos estandarizados a dos componentes para facilitar su visualización y análisis.

Los tres archivos pueden almacenarse en AWS S3 y cargarse desde una API REST para reutilizar los modelos sin necesidad de entrenarlos nuevamente.

## Conclusión personal

Durante esta práctica aprendí a implementar un modelo de aprendizaje no supervisado utilizando K-Means y PCA dentro de una instancia Ubuntu en AWS EC2.

De acuerdo con los resultados obtenidos, se seleccionó un valor óptimo de K = [valor], debido a que presentó el mayor Coeficiente de Silueta, con un resultado de [valor]. También se obtuvo un Índice Davies-Bouldin de [valor], que permite evaluar la separación y compactación de los grupos formados.
