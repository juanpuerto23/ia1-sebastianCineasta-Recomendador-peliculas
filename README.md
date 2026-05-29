# 🎬 Recomendador y Clasificador de Películas — Rotten Tomatoes

**Repositorio:** `ia1-sebastian-recomendacion_peliculas`  
**Curso:** Inteligencia Artificial I — Grupo C2 2026-1  
**Universidad:** Universidad Industrial de Santander (UIS)  
**Autor:** Juan Sebastián Puerto Sánchez — Cód. 2224511

---

## 📌 Descripción del Proyecto

Proyecto de Inteligencia Artificial que aborda la predicción y recomendación de películas
a partir del dataset público de Rotten Tomatoes. Se implementaron técnicas de aprendizaje
supervisado (clasificación) y no supervisado (clustering y reducción dimensional) para
responder la pregunta central:

> ¿Es posible predecir si una película será clasificada como *Fresh*, *Rotten* o
> *Certified Fresh* en Rotten Tomatoes a partir de sus características y reseñas críticas?

---

## 🎥 Video Resumen

> **[⏯ Ver video resumen del proyecto — máx. 5 minutos](#)**  
> *(Reemplazar `#` con el enlace real al video)*

---

## 📂 Estructura del Repositorio
El notebook está organizado en tres partes claramente anotadas con celdas Markdown:

| Parte | Contenido |
|---|---|
| **Parte 1** | Análisis Exploratorio de Datos (EDA) — secciones 1 a 9 |
| **Parte 2** | Preprocesamiento, Aprendizaje Supervisado y Análisis de Resultados — secciones 10 a 19 |
| **Parte 3** | Aprendizaje No Supervisado, Clustering y Reducción Dimensional — secciones 20 a 27 |

---

## 📊 Dataset

### Fuente
**Kaggle — Rotten Tomatoes Movies and Critic Reviews Dataset**  
Autor: [stefanoleone992](https://www.kaggle.com/stefanoleone992)  
🔗 https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset

### Archivos necesarios

| Archivo | Descripción | Tamaño aprox. |
|---|---|---|
| `rotten_tomatoes_movies.csv` | Información de cada película (título, género, duración, director, tomatometer, etc.) | ~17 000 registros |
| `rotten_tomatoes_critic_reviews.csv` | Reseñas individuales de críticos (score, texto, fecha, publicación) | ~1 130 000 registros |

### Instrucciones de descarga

1. Crear una cuenta gratuita en [Kaggle](https://www.kaggle.com) si no tienes una.
2. Ir al dataset: https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset
3. Hacer clic en **Download** (botón azul, esquina superior derecha).
4. Descomprimir el archivo `.zip` descargado.
5. Colocar `rotten_tomatoes_movies.csv` y `rotten_tomatoes_critic_reviews.csv` en el
   mismo directorio donde se ejecute `Proyecto_IA_Final.ipynb`.

> Los archivos **NO están incluidos** en este repositorio por su tamaño.
> El procesamiento inicial de ambos datasets se realiza en las secciones 2 y 10
> del notebook `Proyecto_IA_Final.ipynb`.

---

## 🛠️ Requisitos

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy ipywidgets
```

O en Google Colab (ya incluidas por defecto, excepto ipywidgets):

```bash
!pip install ipywidgets
```

### Versiones principales utilizadas

| Librería | Versión |
|---|---|
| Python | 3.10+ |
| pandas | 2.x |
| scikit-learn | 1.x |
| matplotlib | 3.x |
| seaborn | 0.13.x |

---

## 🤖 Modelos Implementados

### Aprendizaje Supervisado
| Modelo | F1-Macro (baseline) | F1-Macro (optimizado) |
|---|---|---|
| Naive Bayes | — | — |
| Decision Tree | — | — |
| Random Forest ⭐ | — | — |
| SVM | — | — |

> ⭐ Random Forest fue el modelo con mejor desempeño general.

### Aprendizaje No Supervisado
- **PCA** — reducción dimensional y análisis de varianza explicada
- **t-SNE** — visualización no lineal de clusters
- **K-Means** (K=3 y K=4) — clustering con métricas Silhouette, Davies-Bouldin, Calinski-Harabasz
- **DBSCAN** — detección de outliers y clusters de densidad irregular
- **Clustering Jerárquico** (Ward) — dendrograma interpretable

---

## 🎯 Variable Objetivo

`tomatometer_status` — clasificación oficial de Rotten Tomatoes:

| Valor | Significado |
|---|---|
| `Fresh` | ≥ 60% de reseñas positivas |
| `Rotten` | < 60% de reseñas positivas |
| `Certified Fresh` | Fresh con ≥ 80 reseñas y score ≥ 75% |

---

## 📋 Topics del repositorio

`uis-ia1` · `uis-ia1-c2`