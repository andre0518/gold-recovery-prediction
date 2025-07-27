# 🪙 Predicción de recuperación de oro en minería

## 📌 Descripción
Este proyecto tiene como objetivo desarrollar un modelo de *machine learning* para **predecir la cantidad de oro extraído del mineral** en distintas etapas del proceso metalúrgico. El modelo ayudará a la empresa **Zyfra** a optimizar la producción y eliminar parámetros no rentables.

---

## 🛠️ Herramientas utilizadas
- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn
- Métrica personalizada: **sMAPE**

---

## 🧪 Estructura del proyecto

### 1. Preparación de los datos
- Carga de los datasets de entrenamiento, prueba y fuente completa.
- Revisión del cálculo de la recuperación (`rougher.output.recovery`).
- Identificación de columnas no disponibles en `test`.
- Limpieza y tratamiento de valores ausentes.

### 2. Análisis exploratorio (EDA)
- Visualización de concentraciones de metales (Au, Ag, Pb) en distintas etapas.
- Comparación de distribuciones del tamaño de partículas entre `train` y `test`.
- Detección y eliminación de valores anómalos en concentraciones totales.

### 3. Entrenamiento del modelo
- Evaluación de tres modelos:
  - Regresión Lineal
  - Árbol de Decisión
  - Random Forest (mejor desempeño)
- Validación cruzada con 5 folds.
- Métrica utilizada: `sMAPE` y su versión ponderada final.

### 4. Evaluación final en conjunto de prueba
- Se cargó el conjunto completo (`gold_recovery_full.csv`).
- Se compararon las predicciones con las verdaderas recuperaciones.

---

## ✅ Resultados

**Mejor modelo:** `Random Forest Regressor`

| Métrica              | Valor     |
|----------------------|-----------|
| sMAPE Rougher (test) | 9.717     |
| sMAPE Final (test)   | 10.200    |
| **sMAPE Final Score** | **10.079** |

---

## 📂 Dataset

Los datos fueron provistos por Zyfra. Archivos utilizados:
- `gold_recovery_train.csv`
- `gold_recovery_test.csv`
- `gold_recovery_full.csv`

---

## 📌 Conclusión

Se construyó un modelo robusto, con métricas satisfactorias para su uso real en el sector minero. Esta solución permite anticipar el rendimiento de los procesos metalúrgicos y tomar decisiones informadas para maximizar la eficiencia de producción.

---

## 👩‍💻 Autora

**Andreina Moreno**  
[LinkedIn](https://www.linkedin.com/in/andreina-moreno-franco)  
[GitHub](https://github.com/andre0518)