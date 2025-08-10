# Challenge_ONE_Data_Science_Telecom_X_parte_2

Challenge ONE Data Science - Predicción de Abandono de Clientes de Telecomunicaciones

## 1. Motivación / Propósito  
Este proyecto tiene como objetivo anticipar la pérdida de clientes en una empresa de telecomunicaciones, ofreciendo herramientas predictivas para aplicar estrategias de retención más efectivas :contentReference[oaicite:0]{index=0}.

## 2. Qué es este proyecto  
Un análisis completo con pipeline desde la limpieza de datos hasta el despliegue del modelo final (LightGBM), capaz de estimar la probabilidad de abandono (Churn) de los clientes.

## 3. Origen de los datos  
- El dataset original fue procesado hasta generar `datos_tratados.csv`, que contiene variables de clientes, tipo/duración de contrato, facturación y servicio de internet.  
- El preprocesamiento incluyó manejo de valores faltantes, codificación, SMOTE para balanceo y análisis de multicolinealidad.

## 4. Estructura del repositorio
├── Challenge_ONE_Data_Science_Telecom_X_parte_2_Final.ipynb ← Notebook principal con análisis completo
├── datos_tratados.csv ← Datos preprocesados
├── archivo_champion.pkl ← Modelo LightGBM serializado
├── requirements.txt ← Dependencias del entorno (opcional)
└── README.md ← Esta documentación
Mantener una organización clara facilita la colaboración y la comprensión del proyecto :contentReference[oaicite:1]{index=1}.

## 5. Requisitos e instalación  
- **Python 3.x**  
- Recomendado: usar un entorno virtual e instalar dependencias con:
```bash
pip install -r requirements.txt

6. Guía rápida (Quickstart)
import joblib

# Carga del modelo
model = joblib.load("archivo_champion.pkl")

# Preprocesamiento de nuevos datos (debe reflejar el pipeline original)
# X_new = ...

preds = model.predict(X_new)
print(preds)

7. Resultados principales
Modelos evaluados: Regresión Logística, Random Forest, XGBoost y LightGBM.

Métricas clave: Accuracy, Precisión, Recall, F1-score, ROC AUC.

El modelo ganador fue LightGBM.

Factores influyentes identificados: tipo y duración del contrato (mes a mes), facturación y tipo de servicio de internet (especialmente fibra óptica).

8. Análisis y conclusiones
Contratos mensuales presentan mayor riesgo de abandono.
Los niveles de gasto afectan la percepción de valor y satisfacción.
La fibra óptica mostró asociación con patrones de churn.

Estas conclusiones respaldan acciones de retención optimizadas.

9. Roadmap / Mejoras futuras
Implementar tracking de experimentos con MLflow o Weights & Biases.
Modularizar el código para mayor reusabilidad.
Automatizar el pipeline completo (procesamiento, entrenamiento, evaluación y despliegue).
Desplegar el modelo como API o microservicio para uso productivo 
Data Science PM

10. Reconocimientos y referencias
Este proyecto se inspira en plantillas como Cookiecutter Data Science y normas de documentación para proyectos científicos y colaborativos 
Tilburg Science Hub
Gist

11. Licencia
Este repositorio está licenciado bajo MIT License. Permite copiar, modificar y redistribuir respetando los términos especificados.
