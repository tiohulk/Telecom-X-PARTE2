# Telecom-X-PARTE2
Educational
# 📊 Desafío Telecom X: Predicción de Churn  
## Parte 2 – Análisis Predictivo
Estructura
📁 TelecomX_Desafio_Part2/
│
├── 📄 Telecom_x_parte_2_(prueba).ipynb    ← Tu notebook en Colab
├── 📄 README.md                           ← Documentación (este archivo)
├── 📄 informe_ejecutivo.pdf               ← Opcional: resumen para presentación
└── 📄 datos/                              ← Opcional: copia del CSV si no está en Drive
       └── TelecomX_Data_Limpio.csv
> **Nombre del notebook:** `Telecom_x_parte_2_(prueba).ipynb`  
> Proyecto desarrollado en Google Colab para identificar y predecir la cancelación de servicios (churn) en Telecom X.

---

## 🎯 Objetivo

Desarrollar un modelo de machine learning capaz de predecir qué clientes tienen mayor probabilidad de **cancelar su servicio**, con el fin de que la empresa pueda:

- Anticipar la pérdida de clientes.
- Diseñar estrategias de retención personalizadas.
- Reducir el índice de churn y mejorar la fidelización.

---

## 🛠 Tecnologías y Herramientas

- **Google Colab** – Entorno de desarrollo
- **Python 3** – Lenguaje principal
- **Pandas / NumPy** – Limpieza y manipulación de datos
- **Scikit-learn** – Modelos de clasificación
- **Seaborn / Matplotlib** – Visualización de datos
- **imblearn (SMOTE)** – Balanceo de clases
- **Jupyter Notebook** – Formato del entregable

---

## 📊 Flujo del Análisis

1. **Carga y exploración del dataset** (`TelecomX_Data_Limpio.csv`)
2. **Limpieza de datos**:
   - Conversión de `account.Charges.Total` a numérico
   - Codificación de `Churn` a 0 (No) y 1 (Yes)
   - Eliminación de `customerID`
3. **Preprocesamiento**:
   - One-hot encoding para variables categóricas
   - División entrenamiento/prueba (70/30)
   - Balanceo con SMOTE por desequilibrio de clases
4. **Análisis de correlación** con `Churn`
5. **Entrenamiento de modelos**:
   - Random Forest
   - Regresión Logística
6. **Evaluación con métricas**: Accuracy, Precision, Recall, F1, AUC
7. **Interpretación de resultados** e importancia de variables
8. **Conclusión estratégica** con recomendaciones para la empresa

---

## 📈 Hallazgos Clave

- 🔴 El **contrato mensual** es el mayor predictor de churn.
- 🟢 A mayor **antigüedad (`tenure`)** y **gasto total**, menor probabilidad de cancelar.
- 🔴 Los clientes con **fibra óptica** tienen más churn → posible problema de servicio.
- 🟢 Los que usan **pago automático** tienden a quedarse.

---

## 🤖 Modelos Entrenados

| Modelo | AUC | Precisión | Sensibilidad |
|-------|-----|-----------|-------------|
| Random Forest | ~0.85 | ~0.82 | ~0.78 |
| Regresión Logística | ~0.83 | ~0.80 | ~0.75 |

✅ Ambos modelos fueron entrenados y evaluados correctamente.  
✅ Se usó escalado para Regresión Logística y SMOTE para balancear clases.

---

## 💡 Recomendaciones Estratégicas

1. **Ofrecer descuentos por contratos anuales o de 2 años.**
2. **Programa de bienvenida** para clientes nuevos (primeros 3-6 meses).
3. **Alertas tempranas** para clientes con alto riesgo de churn.
4. **Auditar la calidad del servicio de fibra óptica.**
5. **Campañas de retención** personalizadas antes de renovaciones.

---

## ▶️ Cómo Ejecutar el Notebook

1. Abre Google Colab: [https://colab.research.google.com](https://colab.research.google.com)
2. Sube o abre el archivo: `Telecom_x_parte_2_(prueba).ipynb`
3. Monta tu Google Drive (si el CSV está allí):
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
4.Asegúrate de que la ruta al CSV sea correcta:
url = '/content/drive/MyDrive/COLABS/CHALLENGE TELECOM X PARTE
2/TelecomX_Data_Limpio.csv'

## 🙌 Autor
**Rodrigo P.**  
Estudiante del desafío Telecom X – Ciencia de Datos  


---

> ✅ Proyecto listo para entregar y presentar.
