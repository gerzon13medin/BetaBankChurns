# BetaBankChurns

Descripción del proyecto

Los clientes de Beta Bank se están yendo poco a poco cada mes. Dado que es más barato retener a los clientes existentes que adquirir nuevos, el banco busca una solución para anticipar qué clientes están en riesgo de abandonar.

Este proyecto consiste en desarrollar un modelo de Machine Learning que prediga si un cliente dejará el banco próximamente, con el objetivo de ayudar a las áreas de negocio a tomar decisiones preventivas.

⸻

Objetivo
	•	Predecir si un cliente abandonará el banco (Exited).
	•	Maximizar la métrica F1-score (mínimo requerido: 0.59).
	•	Comparar el rendimiento con la métrica AUC-ROC.

⸻

Dataset

Archivo: Churn.csv

Características principales:
	•	RowNumber – índice del registro.
	•	CustomerId – identificador único del cliente.
	•	Surname – apellido.
	•	CreditScore – puntaje crediticio.
	•	Geography – país de residencia.
	•	Gender – sexo.
	•	Age – edad.
	•	Tenure – antigüedad del cliente en el banco (años).
	•	Balance – saldo de la cuenta.
	•	NumOfProducts – número de productos bancarios contratados.
	•	HasCrCard – tarjeta de crédito (1 = sí, 0 = no).
	•	IsActiveMember – actividad del cliente (1 = sí, 0 = no).
	•	EstimatedSalary – salario estimado.

Variable objetivo:
	•	Exited – si el cliente abandonó el banco (1 = sí, 0 = no).

⸻

Metodología
	1.	Preparación y preprocesamiento de datos
	•	Limpieza de valores y verificación de tipos de datos.
	•	Codificación de variables categóricas (Geography, Gender).
	•	Escalado de variables numéricas.
	2.	Exploración de datos
	•	Análisis de distribución de variables.
	•	Verificación del desbalance de clases.
	3.	Modelos iniciales (baseline)
	•	Entrenamiento sin corrección de desbalance.
	•	Evaluación de métricas para establecer referencia.
	4.	Manejo del desbalance de clases
	•	Oversampling (SMOTE).
	•	Undersampling.
	•	Ajuste de pesos de clase en los algoritmos.
	5.	Entrenamiento y validación de modelos
	•	Modelos probados: Logistic Regression, Random Forest, Gradient Boosting.
	•	Búsqueda de hiperparámetros con GridSearchCV.
	•	Evaluación en conjunto de validación.
	6.	Prueba final
	•	Selección del mejor modelo.
	•	Medición de F1-score y AUC-ROC en conjunto de prueba.

⸻

Resultados
	•	Mejor modelo: [especificar, ej. Gradient Boosting]
	•	F1-score (test): [ej. 0.62]
	•	AUC-ROC (test): [ej. 0.84]

El modelo final supera el umbral requerido y demuestra buen poder de discriminación entre clientes que abandonan y los que permanecen.

⸻

🛠️ Tecnologías utilizadas
	•	Python
	•	Pandas, NumPy – manipulación de datos.
	•	Scikit-learn – modelos de Machine Learning y métricas.
	•	Matplotlib, Seaborn – visualización.
