# Predicción del Producto Interno Bruto mediante Regresión Lineal

## Descripción

Proyecto académico de análisis de datos que desarrolla un modelo de regresión lineal múltiple para analizar y predecir el Producto Interno Bruto (PIB) de diferentes países y economías.

El proyecto utiliza indicadores económicos y demográficos correspondientes al año 2023, obtenidos principalmente del Banco Mundial mediante su API de datos. Se aplican procesos de recolección, exploración, limpieza, visualización, modelado y evaluación de datos utilizando Python y Scikit-learn.

## Objetivo

Desarrollar un modelo de regresión lineal múltiple capaz de estimar el Producto Interno Bruto (PIB) a partir de diferentes indicadores económicos y demográficos de países y economías.

### Objetivos específicos

* Obtener datos económicos y demográficos desde una fuente oficial.
* Explorar y comprender las características del conjunto de datos.
* Identificar y eliminar registros correspondientes a agregados regionales o grupos económicos.
* Analizar la relación entre las variables mediante estadísticas y visualizaciones.
* Construir un modelo de regresión lineal múltiple.
* Evaluar el desempeño del modelo mediante métricas estadísticas.
* Analizar los errores y residuos generados por el modelo.
* Documentar el proceso mediante un notebook de Jupyter/Google Colab.

## Fuente de datos

Los datos utilizados fueron obtenidos del **Banco Mundial – World Development Indicators (WDI)** mediante su API.

Los datos corresponden al año **2023** y contienen indicadores económicos y demográficos de diferentes países y economías.

Después del proceso de limpieza se obtuvo un conjunto de datos de **150 observaciones y 8 variables**, sin valores faltantes en las variables seleccionadas.

## Variables utilizadas

### Variable dependiente

* **PIB:** Producto Interno Bruto, expresado en dólares estadounidenses (US$).

### Variables independientes

* **Población:** población total.
* **Exportaciones:** exportaciones de bienes y servicios como porcentaje del PIB.
* **Importaciones:** importaciones de bienes y servicios como porcentaje del PIB.
* **Desempleo:** porcentaje de la población activa.
* **Inflación:** inflación medida mediante la variación porcentual anual del índice de precios al consumidor.

## Metodología

El proyecto se desarrolló mediante las siguientes etapas:

1. Recolección de datos mediante la API del Banco Mundial.
2. Integración de los diferentes indicadores económicos.
3. Exploración inicial del conjunto de datos.
4. Identificación de países, economías y registros agregados.
5. Limpieza del conjunto de datos.
6. Análisis estadístico y exploratorio.
7. Análisis de correlaciones entre variables.
8. División de los datos en conjuntos de entrenamiento y prueba.
9. Construcción del modelo de regresión lineal múltiple.
10. Generación de predicciones.
11. Evaluación mediante MAE, RMSE y R².
12. Análisis de residuos y errores.
13. Visualización de los resultados.
14. Documentación del proyecto.

## Modelo utilizado

Se utilizó un modelo de **Regresión Lineal Múltiple** mediante la clase `LinearRegression` de la biblioteca Scikit-learn.

Las variables utilizadas para realizar las predicciones fueron:

* Población
* Exportaciones
* Importaciones
* Desempleo
* Inflación

La variable objetivo fue el PIB.

Los datos fueron divididos utilizando un **80 % para entrenamiento y 20 % para prueba**, con `random_state=42`.

## Resultados

El modelo fue evaluado utilizando las observaciones correspondientes al conjunto de prueba.

Los resultados obtenidos fueron:

* **MAE:** US$987.607.462.377,57
* **RMSE:** US$2.063.286.354.110,32
* **R²:** 0,6333

El coeficiente de determinación indica que el modelo explica aproximadamente el **63,33 % de la variabilidad del PIB** observada en el conjunto de prueba.

El MAE y el RMSE presentan valores elevados debido a que el PIB está expresado en dólares estadounidenses y existen diferencias importantes en el tamaño económico de las economías analizadas.

Los resultados también muestran las limitaciones de utilizar un modelo lineal sencillo para representar una variable económica con alta variabilidad entre países. Por esta razón, los resultados deben interpretarse dentro del contexto del conjunto de datos y de las variables seleccionadas.

## Análisis de residuos

Se realizó un análisis de los residuos para identificar diferencias entre los valores reales y los valores predichos por el modelo.

Los residuos se analizaron mediante:

* Gráfico de residuos frente al PIB predicho.
* Histograma de residuos.
* Comparación entre PIB real y PIB predicho.

El análisis permitió identificar errores de diferente magnitud entre las economías. También se observaron predicciones con diferencias importantes respecto a los valores reales, lo que evidencia que existen factores económicos adicionales que no están incluidos en el modelo.

## Limitaciones

El modelo presenta algunas limitaciones:

* Los datos corresponden únicamente al año 2023.
* El PIB presenta diferencias muy grandes entre las economías analizadas.
* Se utilizaron únicamente cinco variables explicativas.
* La regresión lineal supone una relación lineal entre las variables.
* Los resultados pueden verse afectados por valores extremos.
* El modelo no debe interpretarse como una relación causal entre las variables.
* El conjunto de prueba contiene 30 observaciones, por lo que los resultados deben interpretarse con cautela.

## Posibles mejoras

Como futuras mejoras del proyecto se podrían considerar:

* Incorporar datos de varios años.
* Utilizar más variables económicas y sociales.
* Aplicar transformaciones logarítmicas al PIB.
* Comparar la regresión lineal con otros algoritmos de Machine Learning.
* Realizar validación cruzada.
* Analizar diferentes técnicas de selección de variables.
* Evaluar modelos no lineales.

## Estructura del repositorio

```text
Proyecto-regresion-pib/
│
├── datos/
│   └── dataset_regresion_pib_2023_limpio.csv
│
├── notebooks/
│   └── regresion_lineal_pib_2023.ipynb
│
├── informe/
│   └── informe_regresion_lineal_pib.pdf
│
└── README.md
```

## Herramientas utilizadas

* Python
* Google Colab
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* API del Banco Mundial
* GitHub

## Fuentes y referencias

### Fuente académica

Universidad de Cundinamarca. *Introducción al Machine Learning: Una Guía Práctica*. Material académico del programa de posgrado.

https://posgrado.ucundinamarca.edu.co/pluginfile.php/79242/mod_label/intro/Introduccion-al-Machine-Learning-Una-Guia-Practica.pdf

### Documentación técnica

Scikit-learn. *Getting Started — scikit-learn 1.9.1 documentation*. Documentación oficial.

https://scikit-learn.org/stable/getting_started.html

### Fuente de datos

World Bank. *World Development Indicators*. Banco Mundial.

### Material audiovisual complementario

Learning Scikit-Learn. YouTube.

https://www.youtube.com/watch?v=rvVkVsG49uU

Tutorial: ¡SCIKIT-LEARN DESDE CERO! YouTube.

https://www.youtube.com/watch?v=qUjIybMkXBs

## Autor

**Yerson Ronaldo Rivas Ruiz**

Administrador de Empresas – Universidad de Cundinamarca.

Estudiante de Especialización en Análisis y Ciencia de Datos.

