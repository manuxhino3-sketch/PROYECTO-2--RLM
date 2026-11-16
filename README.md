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

**Desempeño.** El modelo explica ~64% de la variación del precio en test.
Es un resultado aceptable para un modelo simple con solo 4 variables, pero
el RMSE (~419 €) representa un error considerable respecto al precio medio.

**Variable más influyente.** CPU_frequency tiene un coeficiente de 310 €/GHz:
por cada GHz adicional, manteniendo las demás variables constantes, el precio
predicho aumenta en 310 €. Se trata de una asociación, no de causalidad.
> Nota: para comparar la importancia relativa se recomienda usar coeficientes estandarizados.

**Calidad de las features.** Las variables son predictoras razonables, pero el
R² indica que faltan factores relevantes.

**Train vs. Test.** Las métricas son similares (test ligeramente mejor), lo que
indica que no hay sobreajuste. El R² moderado sugiere más bien que el modelo
es simple (posible subajuste).

## Limitaciones y mejoras futuras
- Incorporar GPU, CPU_company y tipo/capacidad de memoria (SSD/HDD)
- Aplicar log al precio y codificar variables categóricas
- Validación cruzada y comparación con Ridge, Lasso y Random Forest
- Revisar multicolinealidad entre Inches y Weight (VIF)


