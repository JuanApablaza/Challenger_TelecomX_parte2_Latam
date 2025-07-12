# Challenger_TelecomX_parte2_Latam
Segundo Desafio JULIO
📌 Descripción del Proyecto
Este proyecto tiene como objetivo desarrollar modelos predictivos para identificar clientes con alta probabilidad de cancelar sus servicios en Telecom X. El análisis incluye:

Preprocesamiento de datos (limpieza, codificación, normalización).

Selección de variables clave mediante análisis de correlación e importancia.

Entrenamiento de modelos (Regresión Logística, Random Forest, XGBoost, SVM, KNN).

Evaluación de rendimiento con métricas como exactitud, precisión, recall y ROC AUC.

Interpretación estratégica de los factores que influyen en el churn.

🎯 Objetivos
Predecir cancelaciones con al menos un 80% de precisión.

Identificar variables críticas que impactan en la retención de clientes.

Proponer estrategias basadas en datos para reducir el churn.

📊 Estructura del Código
1. Preprocesamiento de Datos
Eliminación de columnas irrelevantes (customerID, fecha_ejemplo).

Conversión de variables categóricas a numéricas (OneHotEncoder).

Normalización de variables numéricas (StandardScaler).

Manejo de valores nulos y desbalanceo de clases.

2. Análisis Exploratorio (EDA)
Matriz de correlación entre variables numéricas.

Visualización de relaciones clave:

Contract vs Churn (gráfico de barras).

MonthlyCharges vs Churn (boxplot).

tenure vs Churn (scatter plot).

3. Modelado Predictivo
Modelos implementados:

Regresión Logística (normalizado).

Random Forest (sin normalización).

XGBoost (para relaciones no lineales).

SVM (kernel lineal).

KNN (basado en distancia).

Métricas de evaluación:

python
print(classification_report(y_test, y_pred))
print("ROC AUC:", roc_auc_score(y_test, y_proba))
4. Interpretación de Resultados
Importancia de variables:

MonthlyCharges (mayor impacto en churn).

Contract_Month-to-month (clientes con contratos cortos son más propensos a cancelar).

OnlineSecurity_No (falta de seguridad aumenta el riesgo).

Curvas de aprendizaje para diagnosticar overfitting/underfitting.

📌 Resultados Clave
Modelo	Exactitud	ROC AUC	Precisión (Churn)	Recall (Churn)
Regresión Logística	78.5%	0.85	72.1%	68.3%
Random Forest	82.3%	0.89	76.5%	74.2%
XGBoost	83.1%	0.90	77.8%	75.6%
Variables más importantes:

MonthlyCharges (100% de importancia).

PaperlessBilling (31.4%).

OnlineSecurity (14.4%).

🚀 Estrategias de Retención Propuestas
Para clientes con cargos altos:

Ofrecer paquetes personalizados con descuentos progresivos.

Incluir servicios premium gratuitos (ej: seguridad en línea).

Para facturación digital:

Rediseñar el portal de autogestión para mejorar la UX.

Implementar recordatorios automáticos por SMS/email.

Para clientes nuevos (tenure < 12 meses):

Programas de onboarding con soporte prioritario.

Descuentos especiales al cumplir 6 meses.

Para clientes sin seguridad en línea:

Promocionar pruebas gratuitas de OnlineSecurity.

Capacitaciones sobre ciberseguridad.

🛠️ Requisitos Técnicos
Librerías:

python
pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost
Datos de entrada:

Archivo CSV con columnas como tenure, MonthlyCharges, Contract, Churn, etc.

Entorno:

Python 3.8+.

Jupyter Notebook o Google Colab.

📂 Estructura de Archivos
text
/TelecomX-Churn-Prediction
│── /data
│   └── datos_tratados.csv          # Dataset preprocesado
│── /notebooks
│   └── churn_analysis.ipynb        # Análisis completo
│── /models
│   └── trained_model.pkl           # Modelo serializado
│── README.md                       # Este archivo
🔍 Conclusiones
El precio (MonthlyCharges) es el principal driver de churn.

Los modelos basados en árboles (Random Forest, XGBoost) superan a la regresión logística.

Acciones recomendadas: Enfocarse en mejorar la percepción de valor y la experiencia digital.

📧 Contacto
Autor: [Tu Nombre]

LinkedIn: [enlace]

GitHub: [enlace]

Nota: Ejecutar el código en el orden secuencial del Jupyter Notebook para evitar errores.
