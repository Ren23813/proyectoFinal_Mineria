# Proyecto Final Minería de Datos (PBL)

**Transformación y Modelado de Indicadores Socioeconómicos en Latinoamérica**

**Integrantes del Equipo:**
- Gerardo Andre Fernandez Cruz 23763
- José Gerardo Ruiz García 23719
- Melisa Dayana Mendizabal Meléndez 23778
- Renato Manuel Rojas Roldan 23813

## 🎯 Objetivo Principal del Proyecto
Convertir un conjunto de datos real, ambiguo y no estructurado de indicadores socioeconómicos de CEPAL en un problema bien definido de Data Mining. El dataset resultante está diseñado para el entrenamiento de algoritmos predictivos que analicen la **adopción y evolución del uso de internet en Latinoamérica** a través del tiempo, segmentado por rango de edad.

---

## 🗂️ Fase 1: Exploración profunda y Formulación (Semana 1)
**Objetivo:** Entender el conjunto de datos original (`data_1777144519.csv`) y proponer un problema central a resolver.
- **Entregables:** Notebook `Fase1ProyectoFinal.ipynb` y documento de justificación.
- **Resumen de Tareas:**
  - Se llevó a cabo un Análisis Exploratorio de Datos (EDA) minucioso utilizando Pandas.
  - Se identificaron problemas estructurales en el dataset original (columnas redundantes de varianza cero, alta presencia de valores faltantes y registros pre-agrupados).
  - Se definió el problema final y la variable objetivo a resolver de forma justificada.

---

## 🛠️ Fase 2: Transformación del Conjunto de Datos (Semana 2)
**Objetivo:** Convertir el conjunto de datos a un formato numérico y limpio, totalmente utilizable por algoritmos de Machine Learning.
- **Entregables:** Notebook `Fase2ProyectoFinal.ipynb` y el dataset procesado `datos_transformados.csv`.
- **Resumen de Tareas:**
  - **Manejo de nulos y limpieza:** Eliminación de variables irrelevantes y constantes (`notes_ids`, `indicator`, `unit`, `source_id`).
  - **Prevención de Multicolinealidad:** Eliminación de la categoría "Total" en grupos etarios para evitar el doble conteo de datos en el modelo predictivo.
  - **Codificación Ordinal:** Mapeo numérico secuencial de los rangos de edad (0 a 4) para conservar la magnitud natural del crecimiento de la edad.
  - **One-Hot Encoding:** Creación de variables *dummy* (binarias) para `País__ESTANDAR`, permitiendo aislar el impacto de cada país sin establecer una jerarquía falsa entre ellos.
- **Estado Actual:** Conjunto de datos 100% numérico y dimensionado, listo para aplicar algoritmos en la fase de modelado.