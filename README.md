# LFW Face Recognition - Filtros y Clasificación con PCA + SVM

Este proyecto explora el impacto de distintos **filtros de preprocesamiento de imágenes** en un sistema de reconocimiento facial basado en aprendizaje supervisado...

Utilizando el dataset **Labeled Faces in the Wild (LFW)**, se implementó un pipeline completo de clasificación de imágenes, con reducción de dimensionalidad mediante **PCA** y clasificación con **SVM**.

---
Nombre: Mario Alberto Tapia Sotelo
Matricula: 202058645
---

## Objetivos

- Aplicar distintos **filtros de preprocesamiento** (Sobel, Gaussiano, Canny) a un subconjunto del dataset LFW...
- Realizar una **clasificación automática** de rostros mediante un modelo SVM...
- Implementar **reducción de dimensionalidad** con PCA para optimizar el rendimiento del clasificador...
- Evaluar y comparar el impacto de cada filtro en la **precisión del modelo**...

---

## Dataset

- **Nombre:** [Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/)
- **Total de imágenes cargadas:** 3,595
- **Número de clases (personas con ≥15 imágenes):** 96

*No se incluye el dataset completo por tamaño. Puedes descargarlo desde el sitio oficial o Kaggle, el link esta en el ipynb*
*Pero subi una muestra que esta en formato de carpeta zip, solo como muestra*

---

## Filtros aplicados

| Filtro         | Descripción breve                           |
|----------------|---------------------------------------------|
| Original       | Imagen original (en escala de grises)       |
| Sobel          | Detección de bordes por gradiente           |
| Gaussiano      | Suavizado con desenfoque para reducción de ruido |
| Canny          | Detección de bordes más agresiva y precisa  |

---

## Modelo utilizado

- **Reducción de dimensionalidad:** PCA (componentes = 150)
- **Clasificador:** SVM con kernel linear y `class_weight='balanced'`
- **Métrica de evaluación:** Accuracy

---

## Resultados

| Filtro         | Accuracy |
|----------------|----------|
| Original       | 33.8%    |
| Sobel          | 32.4%    |
| Gaussiano      | **35.4%**  |
| Canny          | 27.4%    |

---

## Análisis

> El filtro **Gaussiano** obtuvo el mejor rendimiento, probablemente debido a su capacidad para reducir el ruido sin eliminar estructuras relevantes.  
> El filtro **Canny**, si bien detecta bordes con precisión, puede eliminar demasiada información útil para la clasificación.

---

