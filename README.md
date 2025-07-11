# Análisis Exploratorio de Datos (EDA) y Selección de Problema con 
Datos de Pokémon

## Descripción del Proyecto

Este proyecto tiene como objetivo realizar un Análisis Exploratorio de 
Datos (EDA) en varios conjuntos de datos y, basándose en los 
hallazgos, seleccionar una problemática específica de machine learning 
para abordar. Actualmente, el enfoque inicial se ha centrado en un 
conjunto de datos de Pokémon (`pokemon_data.csv`).

## Análisis Exploratorio de Datos (EDA)

Se ha realizado un EDA inicial para el conjunto de datos de Pokémon, 
que incluye:

*   **Carga y exploración de datos:** Carga del archivo CSV y 
visualización de información básica (`.info()`, `.head()`, 
`.describe()`).
*   **Manejo de valores nulos y duplicados:** Identificación y 
tratamiento de valores faltantes (columna 'moves') y verificación de 
filas duplicadas.
*   **Ingeniería de características:** Extracción de estadísticas de 
combate individuales (HP, Ataque, Defensa, etc.) de la columna 
'stats'.
*   **Visualizaciones:** Generación de histogramas para visualizar la 
distribución de variables numéricas y boxplots para identificar 
outliers. Creación de matrices de correlación para entender las 
relaciones entre las variables numéricas y las estadísticas de 
combate.

## Hallazgos Clave del EDA (Pokémon)

*   El conjunto de datos contiene información sobre 1268 Pokémon 
(después de eliminar filas con valores nulos en 'moves').
*   Las columnas 'base_experience', 'height' y 'weight' presentan 
distribuciones sesgadas y con presencia de outliers significativos.
*   Las estadísticas de combate muestran diversas correlaciones entre 
sí.
*   No se encontraron filas duplicadas.

## Diagnóstico y Selección de Problema

Basándose en el EDA del conjunto de datos de Pokémon, se ha 
identificado que predecir la **Experiencia Base (`base_experience`)** 
de un Pokémon es una problemática interesante y adecuada para abordar 
como un problema de **regresión**.

Esta elección se justifica por:

*   La relevancia de la experiencia base en las mecánicas del juego.
*   La disponibilidad de múltiples características numéricas 
(estadísticas, altura, peso) que pueden ser utilizadas como 
predictores.
*   Los desafíos que presenta el dataset, como la presencia de 
outliers y distribuciones sesgadas, que requerirán un manejo adecuado 
durante el modelado.

## Próximos Pasos

*   Completar el EDA para los conjuntos de datos restantes.
*   Documentar detalladamente los hallazgos y diagnósticos para cada 
conjunto de datos.
*   Proceder con el modelado de regresión para predecir la experiencia 
base, incluyendo la selección y evaluación de modelos (KNN, Árbol de 
Decisión, etc.) utilizando validación cruzada.
*   Explorar la ingeniería de características adicionales a partir de 
las columnas categóricas ('types', 'abilities', 'moves').
