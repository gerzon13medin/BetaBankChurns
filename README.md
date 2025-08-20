# BetaBank Churn Prediction  

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)  
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Modeling-orange)  
![Status](https://img.shields.io/badge/Status-Completed-success)  
![F1 Score](https://img.shields.io/badge/F1%20Score-0.62-brightgreen)  
![AUC ROC](https://img.shields.io/badge/AUC--ROC-0.84-blueviolet)  

---
## Descripción del proyecto

Los clientes de Beta Bank se están yendo poco a poco cada mes. Dado que es más barato retener a los clientes existentes que adquirir nuevos, el banco busca una solución para anticipar qué clientes están en riesgo de abandonar.

Este proyecto consiste en desarrollar un modelo de Machine Learning que prediga si un cliente dejará el banco próximamente, con el objetivo de ayudar a las áreas de negocio a tomar decisiones preventivas.

---

## Objetivo

- Predecir si un cliente abandonará el banco (Exited).
- Maximizar la métrica F1-score (mínimo requerido: 0.59).
- Comparar el rendimiento con la métrica AUC-ROC.

---

## Dataset  
**Archivo:** `Churn.csv`  

**Características principales:**  
- `RowNumber` – índice del registro  
- `CustomerId` – identificador único del cliente  
- `Surname` – apellido  
- `CreditScore` – puntaje crediticio  
- `Geography` – país de residencia  
- `Gender` – sexo  
- `Age` – edad  
- `Tenure` – antigüedad en el banco (años)  
- `Balance` – saldo de la cuenta  
- `NumOfProducts` – número de productos bancarios  
- `HasCrCard` – tarjeta de crédito (1 = sí, 0 = no)  
- `IsActiveMember` – actividad del cliente (1 = sí, 0 = no)  
- `EstimatedSalary` – salario estimado  

**Variable objetivo:**  
- `Exited` – cliente abandonó el banco (1 = sí, 0 = no)  

---

## Metodología  

1. **Preparación y preprocesamiento**  
   - Limpieza de valores y tipos de datos  
   - Codificación de variables categóricas (`Geography`, `Gender`)  
   - Escalado de variables numéricas  

2. **Exploración de datos (EDA)**  
   - Distribución de variables  
   - Verificación del desbalance de clases  

3. **Modelos iniciales (baseline)**  
   - Entrenamiento sin corrección de desbalance  
   - Evaluación de métricas de referencia  

4. **Manejo del desbalance**  
   - Oversampling (SMOTE)  
   - Undersampling  
   - Ajuste de pesos de clase en los algoritmos  

5. **Entrenamiento y validación**  
   - Modelos probados: Logistic Regression, Random Forest, Gradient Boosting  
   - Búsqueda de hiperparámetros con **GridSearchCV**  
   - Validación con métricas F1 y AUC-ROC  

6. **Prueba final**  
   - Selección del mejor modelo  
   - Medición de métricas en conjunto de prueba  

---

## Resultados  

- **Mejor modelo:** Gradient Boosting  
- **F1-score (test):** `0.62`  
- **AUC-ROC (test):** `0.84`  

El modelo final **supera el umbral requerido** y demuestra buen poder de discriminación entre clientes que abandonan y los que permanecen.  



## 👨‍💻 Autor  

**Gerzon Medina Ortiz**  
📧 [gerzon13medin@gmail.com](mailto:gerzon13medin@gmail.com)  
💼 [LinkedIn](https://www.linkedin.com/in/gerzon-medina-robotics-datascience)  
