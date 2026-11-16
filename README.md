# REGRESION LINEAL MULTIPLE- ANALISIS DE PRECIOS DE LAPTOPS
##DESCRIPCION
Se desarrollo un model de regresion lineal multiple para predecir los precios de distintas laptops
utilizando variables numericas del dataset https://www.kaggle.com/datasets/ironwolf437/laptop-price-dataset
Las variables numericas utilizadas fueron:
*RAM(GB)
*CPU_frequency(GHz)
*Inches
*Weight(Kg)

##Resultados
Métrica	Train	Test
R²	0.5912	0.6463
MAE	323.72	311.14
RMSE	446.97	419.01

##Conclusiones
- ¿Cuál fue el desempeño del modelo?
  El modelo logro explicar hasta un 64% de la variacion del precio de las laptops utilizando
  las variables numericas ya dichas. Considero que es un numero aceptable pero todavia hay
  una gran variabilidad que no se puede explicar solamente usando estas variables.
- ¿Qué variable fue la más influyente?
  La variable mas influyente fue "CPU_frequency(GHz) con un coeficiente de 310 euros, es decir,
  si los ghz aumentan por 1 y las demas variables se mantienen constantes el precio predecido
  aumenta a 310 euros.
-¿Las features fueron buenas predictoras?
Diria que si ya que explicaron mas de la mitad de variacion de precios del dataset, pero el valor del R²
nos dice que hay otros features importantes que no fueron considerados en el modelo.
  Las variables que considero mejorarian el resultado son:
  -GPU
  -CPU_company
  -Memory(SSD/HDD)
-Comparativa de resultados de evaluación del modelo con los datos de
Entrenamiento y de Test.
Los resultados entre entrenamiento y test fueron bastante similares, pero los numeros son ligeramente
mejores en el test, indicando que no hubo un sobre ajuste.


