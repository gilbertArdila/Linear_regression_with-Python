# 🏠 House Prices Analysis & Linear Regression Model

## 📌 Descripción del Proyecto

Este proyecto consiste en la creación, limpieza, análisis exploratorio y modelado de un dataset sintético de propiedades inmobiliarias con el objetivo de predecir el precio de una vivienda utilizando **regresión lineal**.

El flujo completo sigue un enfoque profesional de análisis de datos:

1. Generación del dataset
2. Limpieza de datos
3. Análisis exploratorio (EDA)
4. Feature Engineering
5. Modelado predictivo

---

## 📊 Dataset

El dataset fue generado artificialmente con aproximadamente **100,000 registros** e incluye variables relevantes del mercado inmobiliario.

### 🔹 Variables principales

| Variable           | Descripción                                     |
| ------------------ | ----------------------------------------------- |
| `price`            | Precio de la vivienda (variable objetivo)       |
| `size_m2`          | Tamaño en metros cuadrados                      |
| `bedrooms`         | Número de habitaciones                          |
| `age`              | Antigüedad de la vivienda                       |
| `distance_city_km` | Distancia al centro de la ciudad                |
| `income`           | Ingreso estimado del comprador                  |
| `location`         | Zona (Centro, Norte, Sur, Occidente)            |
| `date`             | Fecha de registro (formato string inicialmente) |

### ⚠️ Características del dataset

* Contiene valores nulos (~5%)
* Incluye variables categóricas
* Fechas en formato string (requieren transformación)
* Relación lineal simulada para modelado

---

## 🧹 Limpieza de Datos

Se realizaron las siguientes transformaciones:

* Imputación de valores nulos:

  * Variables numéricas → **mediana**
  * Variable categórica → **moda**
* Eliminación o tratamiento de valores nulos en fechas
* Conversión de `date` a tipo datetime
* Corrección de tipos de datos

---

## 📈 Análisis Exploratorio (EDA)

Durante el análisis se evaluó:

* Distribución de variables
* Identificación de outliers
* Correlaciones entre variables
* Relación de cada feature con el precio

### 🔍 Hallazgos clave:

* `size_m2` tiene fuerte correlación positiva con el precio
* `distance_city_km` tiene correlación negativa
* `income` influye positivamente en el precio
* Existen outliers en variables económicas

---

## ⚙️ Feature Engineering

Se realizaron las siguientes transformaciones:

* Extracción de variables temporales:

  * `year`, `month`
* Codificación de variable categórica (`location`)
* Escalado de variables numéricas (StandardScaler)
* Creación de nuevas variables:

  * Relación tamaño/habitaciones
  * Métricas derivadas para análisis

---

## 🤖 Modelo de Regresión Lineal

Se implementó un modelo de regresión lineal utilizando `scikit-learn`.

### 🔹 Proceso:

* Separación en entrenamiento y prueba (80/20)
* Entrenamiento del modelo
* Generación de predicciones

### 📊 Métricas evaluadas:

* **R² (coeficiente de determinación)**
* **RMSE (Root Mean Squared Error)**

---

## 📉 Resultados

El modelo logró capturar correctamente las relaciones lineales del dataset, mostrando:

* Buen nivel de ajuste (R² alto esperado)
* Error promedio controlado (RMSE)
* Coherencia en los coeficientes del modelo

---

## 🧠 Conclusiones

* La regresión lineal es adecuada cuando existe una relación lineal clara entre variables
* La limpieza de datos impacta directamente el rendimiento del modelo
* El feature engineering mejora significativamente la capacidad predictiva
* La interpretación de coeficientes permite entender el comportamiento del negocio

---

## 🚀 Tecnologías utilizadas

* Python 🐍
* Pandas
* NumPy
* Matplotlib / Seaborn
* Scikit-learn

---

## 📂 Estructura del proyecto

```
├── data/
│   └── house_prices_dataset.csv
├── notebooks/
│   └── analysis.ipynb
├── README.md
```

---

## 👨‍💻 Autor: Gilbert Ardila

Proyecto desarrollado como práctica de análisis de datos y machine learning enfocado en regresión.

---

## ⭐ Notas finales

Este proyecto simula un flujo real de trabajo en análisis de datos, desde la generación del dataset hasta la construcción de un modelo predictivo, siguiendo buenas prácticas de la industria.
