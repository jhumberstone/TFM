# Comparación de estrategias de modelos híbridos (ARIMA+LSTM) para la previsión de la demanda de productos
Este repositorio contiene el desarrollo del Trabajo de Fin de Máster (TFM) del Máster en Ciencia de Datos de la Universitat Oberta de Catalunya (UOC). El objetivo principal del proyecto es **comparar el desempeño de tres enfoques de modelos híbridos que combinan ARIMA y LSTM (secuencial, paralelo e integrado) para predecir la demanda de productos**, con el fin de determinar cuál ofrece mayor precisión predictiva en un contexto de gestión de inventarios.

El trabajo incluye desde el análisis exploratorio de datos hasta la implementación de modelos híbridos, incorporando segmentación de series temporales, evaluación de métricas de error y análisis de impacto económico.

## Estructura del repositorio
El repositorio está organizado en notebooks que deben ser consultados en el siguiente orden para seguir la secuencia lógica del proyecto:

### 1. tfm-eda.ipynb
**Análisis exploratorio de datos (EDA)**
Se realiza una exploración inicial de las variables, análisis de valores atípicos, patrones de estacionalidad y rotura de stock. Se establecen las bases para entender la dinámica de la demanda.

### 2. tfm-clustering.ipynb
**Segmentación de productos**
Se aplica un enfoque de clustering jerárquico que combina K-Shape y K-Means para identificar grupos de productos con patrones similares de demanda (regulares e irregulares).

### 3. tfm-demanda-cluster-regular.ipynb
**Modelado de la demanda para productos regulares**
Se entrenan modelos ARIMA y LSTM de forma indiviual y luego se entrenan los modelos híbridos (paralelo, secuencial e integrado) personalizados por producto del clúster regular. Se consideran variables exógenas relevantes y se optimizan hiperparámetros.

### 4.tfm-demanda-irregular-cluster-013.ipynb
**Predicción de demanda para productos irregulares (clústeres 0, 1 y 3)**
Se entrenan modelos ARIMA y LSTM de forma indiviual y luego se entrenan los modelos híbridos (paralelo, secuencial e integrado) personalizados por producto de los clústeres irregulares 0, 1 y 3. Se consideran variables exógenas relevantes y se optimizan hiperparámetros.

### 5. tfm-demanda-irregular-cluster-2.ipynb
**Predicción de demanda para productos irregulares (clúster 2)**
Se entrenan modelos ARIMA y LSTM de forma indiviual y luego se entrenan los modelos híbridos (paralelo, secuencial e integrado) personalizados por producto del clúster irregular 2. Se consideran variables exógenas relevantes y se optimizan hiperparámetros.

### 6. tfm-hibrido-paralelo-global.ipynb
**Modelo híbrido paralelo generalizado**
Se implementa un modelo híbrido paralelo (ARIMA + LSTM) que generaliza la predicción para todos los productos. Se comparan los resultados con otros enfoques y se estima el impacto económico del modelo en la gestión de stock.
