# Predicción del Producto Interno Bruto mediante Regresión Lineal

## Descripción del proyecto

Este proyecto desarrolla un modelo de **regresión lineal múltiple** para analizar la relación entre diferentes indicadores económicos y el Producto Interno Bruto (PIB).

El análisis utiliza información del año **2023** obtenida de los **World Development Indicators del Banco Mundial**.

## Objetivo

Construir y evaluar un modelo de regresión lineal capaz de estimar el PIB de diferentes países y economías a partir de variables económicas y demográficas.

## Variables utilizadas

### Variable objetivo

* **PIB:** Producto Interno Bruto, expresado en dólares estadounidenses.

### Variables predictoras

* **Población**
* **Exportaciones (% del PIB)**
* **Importaciones (% del PIB)**
* **Desempleo (% de la población activa)**
* **Inflación (% anual)**

## Metodología

El proyecto comprende las siguientes etapas:

1. Obtención de los datos mediante la API del Banco Mundial.
2. Integración de los indicadores económicos.
3. Limpieza y selección de países/economías individuales.
4. Exploración y análisis de los datos.
5. Análisis de correlaciones.
6. División de los datos en conjuntos de entrenamiento y prueba.
7. Construcción del modelo de regresión lineal múltiple.
8. Generación de predicciones.
9. Evaluación mediante MAE, RMSE y R².
10. Análisis gráfico de las predicciones y los residuos.

## Resultados del modelo

El modelo fue evaluado utilizando 30 observaciones correspondientes al conjunto de prueba.

* **MAE:** US$987.607.462.377,57
* **RMSE:** US$2.063.286.354.110,32
* **R²:** 0,6333

El coeficiente de determinación indica que el modelo explica aproximadamente el **63,33 % de la variabilidad observada en el PIB** de las economías incluidas en el conjunto de prueba.

Los valores de MAE y RMSE son elevados debido a que el PIB se encuentra expresado en dólares estadounidenses y existen diferencias importantes en el tamaño económico de las economías analizadas.

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
└── README.md
```

## Herramientas utilizadas

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* API del Banco Mundial
* GitHub

## Fuente de datos

Banco Mundial – World Development Indicators (WDI).

Los datos corresponden al año 2023 y fueron consultados mediante la API pública del Banco Mundial.

## Autor

**Yerson Ronaldo Rivas Ruiz**

Especialización en Análisis y Ciencia de Datos
