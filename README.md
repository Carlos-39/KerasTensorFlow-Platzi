# 📉 Customer Churn Prediction with TensorFlow & Keras

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?logo=keras&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

Este repositorio implementa un **modelo de red neuronal para predecir la rotación de clientes (churn)** en una empresa de telecomunicaciones, utilizando el dataset público de **Telco Customer Churn**. El proyecto incluye todo el pipeline: desde la descarga y limpieza de datos hasta el ajuste de hiperparámetros, evaluación con métricas avanzadas y preparación para producción.

> ℹ️ Basado en un curso de **Platzi**, pero con mejoras, documentación detallada y código listo para reutilizar.

---

## 🎯 Objetivo

Predecir si un cliente **dejará (churn = 1)** o **se quedará (churn = 0)** en el servicio, con el fin de:
- Anticipar pérdidas de ingresos.
- Diseñar estrategias de retención personalizadas.
- Automatizar decisiones comerciales con IA.

---

## 🧪 Tecnologías y herramientas

| Herramienta | Uso |
|------------|-----|
| **TensorFlow / Keras** | Construcción y entrenamiento de redes neuronales. |
| **Keras Tuner** | Optimización automática de hiperparámetros (`RandomSearch`). |
| **Pandas / NumPy** | Manipulación y análisis de datos. |
| **Scikit-learn** | Preprocesamiento (`LabelEncoder`, `MinMaxScaler`, `train_test_split`). |
| **Seaborn / Matplotlib** | Visualización de métricas: matriz de confusión, curvas ROC, historial de entrenamiento. |
| **ydata-profiling** | Análisis exploratorio automático (EDA). |
| **TensorBoard** | Monitoreo en tiempo real del entrenamiento. |
| **Kaggle API** | Descarga automatizada de datasets. |

---

## 📁 Contenido del notebook

### 1. **Descarga y preparación del dataset**
- Uso de la API de Kaggle para descargar el dataset `blastchar/telco-customer-churn`.
- Eliminación de columnas irrelevantes (`customerID`) y sesgadas (`gender`).
- Manejo de valores faltantes y transformación de variables categóricas.

### 2. **Preprocesamiento**
- Codificación de variables categóricas con `LabelEncoder`.
- Escalado de variables numéricas (`tenure`, `MonthlyCharges`, `TotalCharges`) con `MinMaxScaler`.
- Guardado de transformadores (`joblib`) para uso en producción.

### 3. **Modelado**
- Diseño de arquitecturas con:
  - **Dropout** para regularización.
  - **Regularización L1/L2** para evitar overfitting.
- Ajuste de hiperparámetros con **Keras Tuner** (`RandomSearch`).
- Uso de **Early Stopping** para detener el entrenamiento cuando ya no mejora.

### 4. **Evaluación**
- **Matriz de confusión** y **classification report**.
- **Curva ROC** y **AUC** para medir discriminación del modelo.
- Análisis de overfitting mediante gráficas de `loss` y `accuracy`.

### 5. **Producción**
- Guardado del modelo en formato `.keras`.
- Función `make_prediction()` para inferencia con nuevos datos.
- Validación robusta: el modelo **rechaza datos fuera de la distribución de entrenamiento**.

### 6. **Bonus**
- Integración con **TensorBoard** para monitoreo avanzado.
- Limpieza automática de metadata de Jupyter para evitar problemas de carga.

---

## 📥 Cómo usar

1. **Clona el repositorio**:
   ```bash
   git clone https://github.com/Carlos-39/customer-churn-prediction-keras.git

2. **Instala dependencias**:
   ```bash
   pip install tensorflow keras scikit-learn pandas matplotlib seaborn ydata-profiling joblib

2. **Ejecuta el notebook**

---

### 💡 Hecho por [Carlos Corrales](https://github.com/Carlos-39)

Estudiante de **Ingeniería de Sistemas** en la **Universidad del Valle (Cali, Colombia)**  
Apasionado por la **Inteligencia Artificial**, **Ciencia de Datos** y el **desarrollo colaborativo**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white&style=flat)](https://www.linkedin.com/in/carlos-daniel-corrales)
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white&style=flat)](https://github.com/Carlos-39)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white&style=flat)](mailto:carlos.corrales.ar21@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF6F00?logo=vercel&logoColor=white&style=flat)](https://TU_PORTAFOLIO)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?logo=instagram&logoColor=white&style=flat)](https://instagram.com/carlosdca_)
