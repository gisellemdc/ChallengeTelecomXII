Sobre el proyecto
Este es mi primer pipeline completo de Machine Learning. El objetivo fue construir modelos predictivos capaces de identificar clientes en riesgo de cancelación en Telecom X, una empresa de telecomunicaciones.
El proyecto es la Parte 2 de un desafío más amplio la Parte I consistió en el análisis exploratorio (EDA) y limpieza de los datos.

🗂️ Estructura del proyecto
├── telecom_x_churn.ipynb       # Notebook principal con todo el código
├── datos_tratados.csv          # Archivo CSV limpio de la Parte 1
└── README.md                   # Este archivo

 
Tecnologías utilizadas
LibreríaUsopandasManejo y transformación de datosnumpyOperaciones matemáticasmatplotlibVisualización de gráficasseabornVisualización avanzada (heatmaps, boxplots)scikit-learnModelos de Machine Learning y métricas

Pipeline del proyecto
1️⃣ Preparación de datos

Carga del CSV tratado en la Parte 1
Eliminación de columnas irrelevantes (customerID)
Encoding de variables categóricas con pd.get_dummies()
Verificación de la proporción de Churn (26.54% cancelaron)
Normalización con StandardScaler para modelos sensibles a escala

2️⃣ Correlación y selección de variables

Matriz de correlación (heatmap) entre variables numéricas
Gráfica de top 15 variables correlacionadas con Churn
Análisis dirigido: tenure y gasto total vs cancelación

3️⃣ Modelado predictivo

División 80% entrenamiento / 20% prueba
Entrenamiento de 3 modelos de clasificación
Evaluación con métricas: Accuracy, Precisión, Recall, F1-Score y Matriz de Confusión

4️⃣ Interpretación y conclusiones

Análisis de importancia de variables por modelo
Conclusión estratégica con recomendaciones de retención


Modelos entrenados
ModeloNormalizaciónAccuracyPrecisiónRecallF1-ScoreRegresión Logística 🥇✅ Sí80.62%66.67%53.62%59.44%KNN (k=5)✅ Sí75.73%54.44%50.94%52.63%Árbol de Decisión❌ No79.13%65.99%43.70%52.58%

La Regresión Logística fue el mejor modelo en todas las métricas.


Principales factores de cancelación
Los 3 modelos coincidieron en las mismas variables más importantes:

 customer.tenure — Los clientes nuevos cancelan mucho más. Los primeros meses son críticos.
 Fiber optic — Clientes con fibra óptica tienen mayor tasa de cancelación.
 Contrato mensual — Sin compromiso de permanencia, es fácil cancelar.
 Cheque electrónico — Este método de pago se asocia con más cancelaciones.
 Cargos mensuales altos — A mayor precio, mayor riesgo de cancelación.


Recomendaciones estratégicas

Programa de bienvenida para clientes nuevos — acompañamiento en los primeros 3 meses
 incentivar contratos anuales con descuentos y beneficios exclusivos
 Mejorar experiencia de Fibra Óptica — investigar la brecha entre expectativas y servicio real
 Promover pagos automáticos en lugar de cheque electrónico
 Ofrecer seguridad online y soporte técnico como prueba gratuita




Nota personal
Este fue mi primer pipeline completo de Machine Learning y aprendí muchísimo en el proceso. Cada error de código fue una lección y cada gráfica que salió bien fue una pequeña victoria. ¡Estoy muy orgullosa de este proyecto! 
