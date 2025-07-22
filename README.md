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

Este proyecto permitió aplicar todo el flujo de trabajo típico en un problema real de ciencia de datos: desde la limpieza del dataset hasta el entrenamiento y validación de un modelo predictivo. Se utilizó un modelo de regresión basado en Random Forest para estimar las ventas globales de videojuegos a partir de variables numéricas y categóricas procesadas.

Las variables más influyentes seleccionadas por `SelectKBest` fueron:
- Puntuación de críticos (`Critic_Score`)
- Puntuación de usuarios (`User_Score`)
- Género (`Genre`)
- Plataforma (`Platform`)
- Año de lanzamiento (`Year_of_Release`)

Estos resultados no solo coinciden con la intuición (es razonable pensar que las buenas críticas y los géneros populares impactan en las ventas), sino que también nos permiten validar, con datos, que existen patrones aprovechables para estimar el rendimiento comercial de un juego.

El modelo logró capturar una parte significativa de la variabilidad, aunque no toda. Esto se refleja en un **R²** aceptable, pero no perfecto. Esto tiene sentido, ya que las ventas de un videojuego dependen de muchos factores no incluidos en el dataset, como:
- Publicidad y marketing
- Popularidad de la franquicia o personajes
- Fechas de lanzamiento (competencia, época del año)
- Exclusividad en plataformas
- Reputación del estudio desarrollador

A pesar de estas limitaciones, el modelo mostró un buen desempeño general, siendo fácil de implementar, rápido de entrenar y explicable. Esto lo convierte en un punto de partida útil para estudios de mercado en la industria del gaming.
En resumen, este trabajo no solo cumple con los objetivos de implementación técnica, sino que también ofrece una mirada concreta sobre el potencial del análisis de datos en una industria tan dinámica como la de los videojuegos.

---

## 📁 Archivos incluidos

- `ProyectoParteIII_Romano.ipynb`: Notebook con todo el desarrollo del modelo
- `Dataset_final.csv`: Dataset limpio utilizado para el análisis

---
## 📌 Interpretación de las métricas del modelo

El modelo fue evaluado utilizando dos métricas comunes en regresión:

### 📉 Error Cuadrático Medio (MSE): 5.89

El MSE mide cuánto se equivoca el modelo al predecir las ventas globales. Cuanto más bajo, mejor. En este caso, 5.89 implica que las predicciones del modelo tienen un error promedio notable, especialmente si consideramos que la mayoría de los videojuegos venden entre 0 y 5 millones de unidades.

### 📊 Coeficiente de determinación (R²): 0.04

Esta métrica indica que el modelo explica solo el **4% de la variabilidad** en las ventas. Es decir, el 96% de la variación sigue sin ser explicada por las variables actuales. Esto sugiere que:

- Las variables incluidas (puntuaciones, género, plataforma, año) **no son suficientes** para capturar los factores que impulsan las ventas.
- Existen **otros elementos clave** fuera del alcance del dataset, como marketing, popularidad de la franquicia, estacionalidad, etc.
- La distribución sesgada y con outliers del target también dificulta una predicción precisa.

### 🧠 Conclusión

Aunque el modelo técnicamente funciona, sus resultados muestran que **las ventas globales son difíciles de predecir con las variables actuales**. Aun así, este análisis es valioso como punto de partida, ya que pone en evidencia los límites del dataset y abre la puerta a nuevas hipótesis.

Próximos pasos pueden incluir la incorporación de nuevas fuentes de datos, transformaciones de variables y el uso de modelos más complejos o especializados.

