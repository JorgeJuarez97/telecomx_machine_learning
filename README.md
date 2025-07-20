# Predicción de Cancelación de Clientes - Telecom X

Este proyecto tiene como objetivo principal **predecir el churn (cancelación) de clientes** en una empresa de telecomunicaciones. A través del análisis de datos y modelado predictivo, se busca identificar los factores más influyentes en la decisión de cancelar los servicios y proponer estrategias de retención efectivas.

---

## 📁 Estructura del Proyecto

- `TelecomX_machine_learning.ipynb`: Cuaderno principal en Google Colab donde se desarrolla todo el análisis, desde la limpieza hasta la predicción.
- `dados_tratados.csv`: Dataset tratado y limpio utilizado como base para el modelado (debe estar en la misma carpeta que el cuaderno).
- `README.md`: Este archivo de documentación.

---

## 🔍 Proceso de Análisis y Preparación de Datos

### 1. Carga y tratamiento inicial
- Se parte de un conjunto de datos previamente tratado y guardado como CSV.
- Se eliminan columnas irrelevantes como identificadores o datos redundantes.

### 2. Codificación de variables
- Variables categóricas se convierten a formato numérico mediante técnicas de encoding.

### 3. Balanceo de clases
- Se identificó un desbalance importante en la proporción de clientes que cancelan.
- Se aplicaron dos métodos:
  - **SMOTE (oversampling)**
  - **NearMiss (undersampling)**

### 4. Normalización
- Los datos fueron normalizados para mejorar el rendimiento de modelos sensibles a la escala, como KNN.

---

## 🤖 Modelado Predictivo

### Separación de datos
- Los datos fueron divididos en **conjunto de entrenamiento (train)** y **conjunto de prueba (test)**, usando un 80-20 de split.

### Modelos entrenados
- **K-Nearest Neighbors (KNN)** con SMOTE y NearMiss.
- **Random Forest Classifier** con SMOTE y NearMiss.
- Búsqueda de hiperparámetros con **GridSearchCV** para optimizar el Random Forest.

### Métricas de evaluación utilizadas:
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **Matriz de Confusión**
- **Curva ROC**
- **Curva Precision-Recall**

---

## 📊 Análisis Exploratorio de Datos (EDA)

Durante el análisis se generaron diversos gráficos para obtener insights:

- **Gráfico de distribución del gasto total según churn**.
- **Proporción de cancelación por tipo de contrato**.

---

## 🧠 Principales Insights

- **Clientes con contrato mensual** tienen mayor probabilidad de cancelar.
- **Mayor gasto total** se asocia con menor tasa de churn.
- La variable **"Contract"** resultó ser una de las más influyentes según el modelo Random Forest.

---

## 🛠️ Instrucciones para Ejecutar el Cuaderno

1. **Abre el archivo `TelecomX_machine_learning.ipynb`** en [Google Colab](https://colab.research.google.com) o en tu entorno local.

2. **Instala las bibliotecas necesarias** (en Google Colab, ya están preinstaladas, pero en tu entorno local puedes usar):
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn plotly
   ```

3. **El archivo `dados_tratados.csv`** ya esta cargado con la url del repositorio.

---

## ✅ Resultados

El mejor desempeño lo obtuvo el modelo **Random Forest con datos balanceados por SMOTE**, logrando un excelente equilibrio entre precisión y recall. Se destaca su capacidad de generalización y su interpretación clara gracias a la evaluación de importancia de variables.

---

## 📌 Conclusión Estratégica

A partir de los resultados, se pueden diseñar estrategias específicas de retención, como:

- Ofrecer beneficios a usuarios con contrato mensual para migrar a planes más largos.
- Identificar a los clientes con gastos bajos y promover servicios adicionales.
- Priorizar la atención a clientes en los grupos con mayor propensión al churn, según el modelo predictivo.

---

## 🧑‍💻 Autor

Proyecto desarrollado en el contexto de estudio de ciencia de datos y aprendizaje automático, con fines de análisis y mejora de estrategias comerciales basadas en datos.

---

## 🤝 Contribuciones

Si tienes sugerencias o mejoras, no dudes en abrir un *issue* o enviar un *pull request*.

## 📞 Contacto

* **Correo Electrónico:** [jorgejuarez0407@gmail.com]
* **LinkedIn:** [https://www.linkedin.com/in/jorge-d-juarez/]
