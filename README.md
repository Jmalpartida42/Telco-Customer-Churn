# Customer Churn Analysis | Telco Dataset

Este proyecto realiza un análisis predictivo del abandono de clientes utilizando el dataset de **Telco Customer Churn de Kaggle**. El objetivo principal es identificar patrones de comportamiento y desarrollar un modelo capaz de predecir qué usuarios tienen mayor probabilidad de cancelar su servicio.

---

## 🔍 Análisis Exploratorio de Datos (EDA)

Para entender qué variables influyen realmente en el Churn, realicé un análisis estadístico riguroso:

* **Variables Categóricas:** Utilicé la prueba de **Chi-cuadrado ($\chi^2$)** para medir la dependencia entre las categorías (como tipo de contrato,método de pago,entre otros) y la variable objetivo (Churn).
* **Variables Numéricas:** Apliqué pruebas de **T-Student** para comparar las medias de variables como el `MonthlyCharges` y `Tenure` entre clientes que se quedaron y los que se fueron.
* **Visualización:** Implementé visualizaciones avanzadas (Matplotlib/Seaborn) para validar los hallazgos estadísticos y observar la distribución del riesgo.
---

## 🛠️ Ingeniería de Características

Tras el EDA, preparé los datos para los modelos de Machine Learning:
* Encoding de variables categóricas.
* Escalado de variables numéricas.
* Tratamiento de valores ausentes y desbalanceo de clases.
---

## 🤖 Comparativa de Modelos

Entrené y evalué tres arquitecturas distintas para encontrar la solución óptima:

| Modelo | Ventajas | Desempeño (Recall categoria 1) |
| :--- | :--- | :--- |
| **Random Forest** | Excelente interpretabilidad y manejo de outliers.| *59%* |
| **XGBoost** | Alta precisión mediante Boosting de gradiente. | *70%* |
| **Red Neuronal** | Capacidad para detectar patrones complejos no lineales. | *78%* |

### 🏆 Selección del Modelo
Tras comparar las métricas (priorizando el **Recall** para minimizar los falsos negativos en la fuga de clientes), el modelo seleccionado como mejor opción fue el de **Red Neuronal**.

---

## 🚀 Cómo usar este repositorio
