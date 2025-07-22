# Proyecto Final – Ciencia de Datos 🎮📊

Este proyecto forma parte del módulo final del curso de Ciencia de Datos. El objetivo es aplicar técnicas de aprendizaje automático para predecir las **ventas globales de videojuegos (`Global_Sales`)** a partir de variables como puntuaciones, género, plataforma y año de lanzamiento.

---

## 🧠 Objetivo del Proyecto

Predecir el rendimiento comercial de un videojuego utilizando un modelo de regresión entrenado sobre un dataset histórico, aplicando:

- Selección de características (Feature Selection)
- Modelado supervisado (Random Forest)
- Validación de resultados con métricas de evaluación

---

## 🧾 Dataset

El conjunto de datos contiene información de más de 16.000 videojuegos, incluyendo:

- Nombre del juego
- Plataforma
- Género
- Año de lanzamiento
- Puntuación de críticos (`Critic_Score`)
- Puntuación de usuarios (`User_Score`)
- Ventas por región y ventas globales

📁 Archivo utilizado: `Dataset_final.csv`

---

## ⚙️ Algoritmos y Técnicas Utilizadas

- **Preprocesamiento**: eliminación de nulos, codificación de variables categóricas, transformación de datos
- **Feature Selection**: `SelectKBest` con `f_regression`
- **Modelo**: `RandomForestRegressor` de `sklearn`
- **Métricas**:
  - Error cuadrático medio (MSE)
  - Coeficiente de determinación (R²)

---

## 📊 Resultados

El modelo logró explicar una parte significativa de la variabilidad en las ventas, mostrando que las variables más influyentes son:

- `Critic_Score`
- `User_Score`
- `Genre`
- `Platform`
- `Year_of_Release`

---

## 📝 Conclusiones

El análisis confirma que las puntuaciones de críticos y usuarios, junto con características del juego, pueden ayudar a predecir su éxito comercial. Sin embargo, se sugiere explorar mejoras como ajuste de hiperparámetros, uso de modelos avanzados (XGBoost, LightGBM), o incorporar variables externas (marketing, franquicias).

---

## 📁 Archivos incluidos

- `ProyectoParteIII_Romano.ipynb`: Notebook con todo el desarrollo del modelo
- `Dataset_final.csv`: Dataset limpio utilizado para el análisis

---
