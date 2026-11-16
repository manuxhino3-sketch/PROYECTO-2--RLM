# Regresión Lineal Múltiple: Predicción de Precios de Laptops

Modelo de regresión lineal múltiple para predecir el precio (€) de laptops a partir
de variables numéricas. Dataset: [Laptop Price Dataset (Kaggle)](https://www.kaggle.com/datasets/ironwolf437/laptop-price-dataset)

## Variables utilizadas
| Variable | Descripción |
|---|---|
| RAM (GB) | Memoria RAM |
| CPU_frequency (GHz) | Frecuencia del procesador |
| Inches | Tamaño de pantalla |
| Weight (Kg) | Peso |

## Metodología
- Split train/test: 80/20 (`random_state=42`)
- Estandarización de variables
- Modelo: `LinearRegression` (scikit-learn)

## Resultados
| Métrica | Train | Test |
|---|---|---|
| R² | 0.5912 | 0.6463 |
| MAE (€) | 323.72 | 311.14 |
| RMSE (€) | 446.97 | 419.01 |

## Conclusiones

**Desempeño.** El modelo logro explicar hasta un 64% de la variacion del precio de las laptops 
utilizando las variables numericas ya dichas. Considero que es un numero aceptable pero todavia 
hay una gran variabilidad que no se puede explicar solamente usando estas variables.

**Variable más influyente.** La variable mas influyente fue "CPU_frequency(GHz) con un 
coeficiente de 310 euros, es decir,si los ghz aumentan por 1 y las demas variables 
se mantienen constantes el precio predecido aumenta a 310 euros.

**Calidad de las features.** Las variables son predictoras razonables, pero el
R² indica que faltan factores relevantes como: GPU, CPU_company, Memory(SSD/HDD)

**Train vs. Test.** Los resultados entre entrenamiento y test fueron bastante similares, 
pero los numeros son ligeramente mejores en el test, indicando
que no hubo un sobre ajuste.


