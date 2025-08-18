# TelecomX_Parte2
# Informe de Clasificación de Cancelación de Clientes

🧠 Objetivos del Desafío

- Preparar los datos para el modelado (tratamiento, codificación, normalización).

- Realizar análisis de correlación y selección de variables.

- Entrenar dos o más modelos de clasificación.

- Evaluar el rendimiento de los modelos con métricas.

- Interpretar los resultados, incluyendo la importancia de las variables.

- Crear una conclusión estratégica señalando los principales factores que influyen en la cancelación.

# Predicción de Churn (Telco)

Proyecto de aprendizaje automático para **predecir la cancelación de clientes (churn)**, entender **drivers clave** y proponer **estrategias de retención**.


## 📁 Estructura
.
├─ Telecom_2.ipynb # Colab con todo el flujo
└─ README.md

## 🚀 Ejecución

1. Abre Telecom_2.ipynb en Google Colab.

2. Ejecuta las secciones en orden


## 🧪 Metodología

Target: Churn (binario), en el dataset one-hot se usa onehotencoder__Churn_Yes.

Desbalance: ~73% No Churn / 27% Churn (moderado).

## Modelos:

 - Regresión Logística (baseline, interpretable)

 - Random Forest (ensamble, robusto a escalas/outliers)

Evaluación: Accuracy, Precision, Recall, F1, Matriz de Confusión.

## 📊 Resultados (clase positiva = Churn)
Modelo 	Accuracy	Precision	Recall	F1
Random Forest	~0.794	~0.648	~0.492	~0.559
Regresión Logística	~0.798	~0.650	~0.530	~0.580

# Conclusión: Ambos modelos rinden similar en accuracy, pero Regresión Logística ofrece mejor Recall para Churn, por lo que detecta más bajas reales y es preferible como motor de campañas preventivas.

# 🔎 Variables más relevantes

- Tenure (antigüedad): fuertemente protector (↓ churn).

- Contract Month-to-month: ↑ churn; contrato 1–2 años: ↓ churn.

- Cargos (Total/Mensual): valores altos ↑ churn.

- InternetService = Fiber optic: asociado a ↑ churn.

- TechSupport = No: ↑ churn.

## 🧠 Recomendaciones de retención

- Fidelización temprana (0–6 meses).

- Incentivar contratos de 1–2 años.

- Revisión de precios/planes en segmentos con cargos altos y/o fibra.

- Soporte técnico proactivo (prevención y SLA).

- Campañas dirigidas por score (modelo con mejor Recall).
