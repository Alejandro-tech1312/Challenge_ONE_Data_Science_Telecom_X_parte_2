# Challenge_ONE_Data_Science_Telecom_X_parte_2

Challenge ONE Data Science - Predicción de Abandono de Clientes de Telecomunicaciones
Este repositorio contiene el análisis y los modelos predictivos desarrollados como parte del Challenge ONE Data Science, enfocado en predecir el abandono de clientes (Churn) para una empresa de telecomunicaciones.

El objetivo principal fue construir un pipeline robusto para prever qué clientes tienen una mayor probabilidad de cancelar sus servicios, permitiendo a la empresa anticiparse al problema del abandono y diseñar estrategias de retención dirigidas.

Contenido del Repositorio
notebook_challenge_one.ipynb: El notebook de Google Colab que documenta todo el proceso, desde la preparación inicial de los datos hasta el modelado predictivo y el análisis de resultados.

datos_tratados.csv: Archivo CSV con los datos preprocesados utilizados en el análisis.
lgbm_champion_model.pkl (renombrado como archivo_champion): El modelo Champion guardado (LightGBM), listo para ser cargado y utilizado para hacer predicciones.

Pasos Realizados en el Notebook
El notebook notebook_challenge_one.ipynb sigue un flujo de trabajo estándar de ciencia de datos:

Carga y Exploración Inicial de Datos: Carga del dataset y una primera mirada a su estructura, tipos de datos y valores faltantes.

Preparación y Limpieza de Datos:

Manejo de valores faltantes o inconsistentes.
Eliminación de columnas irrelevantes.
Codificación de variables categóricas (One-Hot Encoding).
Verificación del balance de clases y aplicación de técnicas de balanceo (SMOTE).
Análisis de Multicolinearidad (VIF).
Análisis Exploratorio Adicional: Visualizaciones para entender la distribución de las variables y su relación con el abandono (ej. duración del contrato vs abandono).

Modelado Predictivo: Entrenamiento de varios modelos de clasificación:
Regresión Logística
Random Forest
XGBoost
LightGBM

Evaluación de Modelos: Comparación del rendimiento de los modelos utilizando métricas clave como Accuracy, Precision, Recall, F1-score y ROC AUC, así como matrices de confusión.
Análisis de Importancia de Variables: Identificación de los factores más influyentes en la predicción del abandono para cada modelo.

Conclusiones e Implicaciones Estratégicas: Resumen de los hallazgos clave y propuesta de estrategias de retención basadas en los resultados.
Guardado del Modelo Champion: Serialización y guardado del modelo con mejor rendimiento (LightGBM).

Factores Clave de Abandono Identificados
El análisis reveló que los factores con mayor influencia en la probabilidad de abandono incluyen:

Duración del Contrato: Contratos más cortos (mes a mes) están fuertemente asociados con el abandono.
Tipo de Contrato (Mes a Mes): Es un predictor muy importante de Churn.
Cobro Mensual y Total: Indican el nivel de gasto y pueden estar relacionados con la percepción de valor o la insatisfacción.
Servicio de Internet: Específicamente, el servicio de Fibra Óptica mostró relación con el abandono en algunos modelos.

Uso del Modelo Champion
El modelo guardado (lgbm_champion_model.pkl - renombrado como archivo_champion) puede ser cargado en un entorno Python para hacer predicciones sobre nuevos datos de clientes.
