# Assignment 4: Single-Neuron Network with and without PCA

**Universidad de Monterrey**
**Curso:** Inteligencia Artificial II
**Docente:** Dr. Andrés Hernández Gutiérrez
**Estudiantes:** Jorge Serangelli · Aldo Peña · Jerónimo López
**Fecha:** 05 de marzo de 2026

## Descripción

Clasificación binaria con una neurona única (regresión logística) para predecir si un cliente de un banco portugués suscribirá un depósito a plazo fijo, utilizando el dataset [Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing) de UCI. Se compara el rendimiento del modelo entrenado con las features originales contra uno entrenado con componentes principales (PCA).

## Contenido del Notebook

1. **Introducción al Problema Real** — Descripción del dataset y análisis exploratorio
2. **Diseño y Entrenamiento del Modelo** — Neurona única con 39 features (tras One-Hot Encoding)
3. **Curvas de Aprendizaje** — Diagnóstico de convergencia y generalización
4. **Evaluación en Datos de Prueba** — Matriz de confusión y métricas (Accuracy, Precision, Recall, F1)
5. **Guardado del Modelo** — Exportación en formato `.keras`
6. **Análisis de Componentes Principales (PCA)** — Reducción de dimensionalidad al 95% de varianza
7. **Entrenamiento con Features PCA** — Mismo modelo con entrada reducida
8. **Comparación de Rendimiento** — Tabla y gráficos comparativos entre ambos modelos
9. **Conclusiones Personales**

## Dataset

- **Fuente:** [UCI Machine Learning Repository — Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing)
- **Archivo necesario:** `bank-full.csv` (debe colocarse en la raíz del proyecto)
- **Registros:** 45,211
- **Variable objetivo:** `y` (yes/no — suscripción a depósito a plazo fijo)

## Requisitos

- Python 3.10+
- Dependencias listadas en `requirements.txt`

### Instalación

```bash
pip install -r requirements.txt
```

## Uso

Abrir y ejecutar el notebook `Assignment4_SingleNeuron_PCA.ipynb` de forma secuencial.

## Resultados Principales

| Modelo | Features | Accuracy | Precision | Recall | F1-Score |
|--------|----------|----------|-----------|--------|----------|
| Original | 39 | 0.8426 | 0.41 | 0.83 | 0.55 |
| PCA | 32 | 0.8388 | 0.41 | 0.82 | 0.55 |

El modelo original sin PCA presenta mejor desempeño y mayor interpretabilidad, por lo que es el recomendado para producción.

## Referencias

UCI Machine Learning Repository. (2012). *Bank Marketing Data Set*. University of California, Irvine. https://archive.ics.uci.edu/dataset/222/bank+marketing
