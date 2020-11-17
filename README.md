# MLPortfolio
Portfolio de Machine Learning
# [Caso de estudio: Predicción de enfermedad del corazón](https://github.com/IgnacioPuchet/MLPortfolio/tree/main/heartdisease)

El objetivo del caso de estudio es ayudar al realizar un diagnóstico acertado sobre 
una enfermeddad del corazón a partir de distintas bases de datos que contienen datos 
históricos sobre pacientes de distintas instituciones médicas.

<a href="heartdisease/index.html">Ver..</a>


# [Caso de estudio: Insuficiencia Cardíaca](https://github.com/IgnacioPuchet/MLPortfolio/tree/main/heartfailure)

En este caso de estudio se intenta predecir la probabilidad de que un paciente fallezca luego de haber sufrido una insuficiencia cardíaca.
Este es un tema relevante en la actualidad ya que las muertes causadas por insuficiencia cardiaca han aumentado un 38% en el periodo comprendido 
entre 2011 y 2017 según un estudio publicado en la revista médica JAMA Cardiology de Estados Unidos por lo tanto conocer el impacto que puedan tener distintas 
caracteristicas que se presentan en pacientes que hayan sufrido insuficiencia cardíaca puede ser fundamental para prevenir muertes en poblaciones de riesgo.
<a href="heartfailure/index.html">Ver..</a>

## Composición del dataset 
El dataset fue recolectado por la Government College University de Pakistan.

[Ver dataset](https://archive.ics.uci.edu/ml/datasets/Heart+failure+clinical+records)

Los atributos que componen el dataset son los siguientes:
- edad: edad del paciente en años(entero)
- anemia: disminución de glóbulos rojos o hemoglobina (binomial)
- presión arterial alta: el paciente tiene hipertensión (binomial)
- creatinina fosfoquinasa (CPK): nivel de la enzima CPK en sangre en mcg/L(entero)
- diabetes: el paciente tiene diabetes (binomial)
- fracción de eyección: porcentaje de sangre que sale del corazón en cada contracción (porcentaje entero)
- plaquetas: plaquetas en sangre se mide en kiloplaquetas/ml(real)
- sexo: mujer u hombre (binomial)
- creatinina sérica: nivel de creatinina sérica en sangre en mg/dl(real)
- sodio sérico: nivel de sodio sérico en sangre se mide en mEq/L(entero)
- tabaquismo: si el paciente fuma o no (binomial)
- tiempo: período de seguimiento en días luego de la insuficiencia(entero)
- Muerte (variable objetivo): el paciente falleció durante el período de seguimiento (binomial)

Observando los datos en rapid miner se puede ver que la mayoría de los atributos numericos tienen una distribución casi normal(edad, fracción de eyección, sodio sérico, plaquetas) sin observarse valores fuera de lo común sin embargo en los atributos de creatinina fosfoquinasa y creatinina sérica se detecta una distribución exponencial con la mayoria de los valores cercanos a 0.

![](/heartfailure/creatininaFosfo.PNG)
![](/heartfailure/serumCretinina.PNG)

Con respecto a la variable objetivo los resultados dan que 203(aproximadamente un 68%) de los pacientes sobrevive luego de sufrir una insuficiencia cardíaca y los restantes 96(aproximadamente 32%) fallecen dentro del período de seguimiento.


## Preparación de datos
Inicialmente no se descarta ningún atributo al no encontrar ninguno que pueda ser irrelevante para el resultado final.
No se detectan datos faltantes.
El 70% de los datos se destinan a entrenamiento y el restante 30% a testeo del modelo.

## Modelo utilizando árboles de decisión

![](/heartfailure/modelDT.PNG)

### Rendimiento del entrenamiento

![](/heartfailure/PerformanceTraining.PNG)

### Rendimiento del test

![](/heartfailure/PerformanceTest.PNG)


