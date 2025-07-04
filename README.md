## Predicción del Riesgo de Diabetes Tipo 2 — Proyecto de Certificación KNIME (BEDU)

El objetivo fue construir un modelo de clasificación para predecir el riesgo de desarrollar diabetes tipo 2 utilizando flujos de trabajo en KNIME Analytics Platform.

**Objetivos del Proyecto:**

* Detectar de forma temprana a personas en riesgo de diabetes tipo 2.
* Aplicar técnicas de aprendizaje automático supervisado (clasificación binaria).
* Diseñar un flujo de trabajo completo en KNIME: limpieza, transformación, modelado y visualización.
* Utilizar herramientas de evaluación para validar el rendimiento del modelo.

**Descripción del Conjunto de Datos:**

El dataset contiene variables clínicas, demográficas y de estilo de vida relevantes, como:

* Edad, IMC, niveles de glucosa e insulina.
* Actividad física, tabaquismo, hábitos dietéticos.
* Salud pancreática, tolerancia a la glucosa.
* Datos de embarazo y antecedentes familiares.

La variable objetivo riesgo_diabetes se generó mediante el nodo Rule Engine, considerando:

$niveles_glucosa$ ≥ 140 → 1
$tolerancia_glucosa$ = "Abnormal" → 1
Caso contrario → 0

**Flujo de Trabajo Implementado en KNIME**
* **Limpieza y Transformación**
* **Column Rename (Regex):** Normalización de nombres
*  **Missing Value / Column Filter:** Manejo de valores nulos y columnas irrelevantes
*  **Normalizer:** Escalado de variables numéricas.

**Modelado**

* **Partitioning (70/30):** Estratificación por riesgo.
* **Tree Ensemble Learner (Random Forest):** Modelo robusto para clasificación binaria
* **Tree Ensemble Predictor:** Aplicación del modelo al set de prueba.

**Evaluación y Visualización**

* **Scorer:** Evaluación del modelo (accuracy, recall).
* **Scatter Plot:** IMC vs Niveles de Insulina.
* **Bar Chart:** Comparación de variables clave según la predicción.

**Resultados y Conclusiones**

* El modelo predijo correctamente la mayoría de los casos de riesgo.
* Las variables con mayor impacto: niveles de glucosa, IMC, insulina y edad
* Las visualizaciones reforzaron los hallazgos del modelo y facilitan la interpretación clínica.

**Habilidades Desarrolladas**

* Flujo completo de Machine Learning en KNIME.
* Clasificación supervisada (Tree Ensemble).
* Transformación y limpieza de datos sin programación.
* Evaluación de modelos y visualización efectiva.
* Interpretación de resultados clínicos y presentación visual.

**Herramientas Utilizadas**

* KNIME Analytics Platform

**Componentes principales:**
* Rule Engine
* Partitioning
* Tree Ensemble Learner
* Predictor
* Scorer
* Scatter Plot
* Bar Chart
* Normalizer

Este proyecto evidencia el uso práctico de KNIME para resolver problemas de clasificación médica, aplicando lógica clínica y flujos estructurados de aprendizaje automático sin escribir código.
