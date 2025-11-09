# Predicción de Hábito de Fumar mediante Modelos de Machine Learning

Este proyecto se realizó como parte del Módulo 2 de la Diplomatura en Inteligencia Artificial. El objetivo fue construir un modelo capaz de predecir si una persona es fumadora o no, utilizando datos clínicos y demográficos.

---

## 📊 Objetivo

A partir de un dataset con información médica básica, se entrenaron y compararon distintos modelos de clasificación para predecir la variable objetivo:

- `Smoking` → 0 (No Fumador) / 1 (Fumador)

---

## 🧹 Preprocesamiento y Transformaciones

1. Se analizaron las variables presentes en el dataset.
2. Se convirtió a formato numérico las variables categóricas mediante `LabelEncoder`.
3. Se aplicó **escalado** de las variables para garantizar que los modelos basados en distancia (como KNN y SVM) no se vieran afectados por diferencias de magnitud entre atributos.
4. Se dividió el dataset en conjuntos de entrenamiento y prueba (`train/test split`).

---

## 🤖 Modelos Entrenados

Se entrenaron los siguientes modelos:

| Modelo | Evaluado |
|-------|:--------:|
| Regresión Logística | ✅ |
| Árbol de Decisión | ✅ |
| Random Forest | ✅ |
| K-Nearest Neighbors | ✅ |
| SVM | ✅ |
| Gradient Boosting | ✅ |

Luego se realizó **tuning de hiperparámetros** para optimizar su desempeño.

---

## 🏆 Modelo Seleccionado

El modelo con mejor rendimiento fue:

### **Random Forest (Tuned)**

- Mostró el mejor equilibrio entre **Precisión, Recall y F1-Score**
- Presentó **mejor capacidad generalizadora**
- Se mantuvo estable frente a variaciones en los datos

Este modelo fue usado para realizar la predicción final sobre un segundo dataset.

---

## 🔍 Predicción sobre Nuevos Datos

Se descargó un segundo archivo con nuevos registros.  
Se aplicaron las mismas transformaciones utilizadas durante el entrenamiento, y se generó una columna final:

