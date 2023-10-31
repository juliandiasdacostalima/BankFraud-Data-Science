# Data-Science

Desarrollo del proyecto
A partir de una base de datos de clientes de un banco, la cual con tiene poco más de 300.000 registros y 122 variables [Anexo 1], 
se busca identificar características de personas que cometen fraude, con fraude nos referimos a dificultades o incumplimientos al momento de realizar los pagos de préstamos.
Dentro de esta base de datos podemos encontrar variables que tendrán una gran importancia, como sueldo, estado civil, cantidad de hijos, educación,
mientras que habrá otras variables que son propias del cliente pero tienen menor significancia, por ejemplo, hora en la que pidió el préstamo.
Además, el proyecto tiene un segundo objetivo que es realizar un modelo que pueda predecir el incumplimiento de los pagos a partir de una probabilidad y las variables dadas en el modelo.
  
  Tanto como para el primer objetivo y el segundo, es necesario realizar una limpieza en el dataset, esto se realizó en diferentes pasos:
 Limpieza de variables: En este paso se quitaron las variables que intuí que no tendrían significancia en el modelo.
 Limpieza de valores nulos: En la mayoría de los casos se eliminaron los datos, ya que si consideré que 160.000 registros (luego de la limpieza) 
  serían suficientes para en análisis y la predicción.
 Limpieza de outliers: Se quitaron los outliers, es decir valores que estaban por fuera del diagrama de caja.
 Arreglos de variables: En este punto algunas de las variables numéricas binarias se cambiaron en Si/No, o en el caso de género en Masculino y femenino para poder graficar.
  Luego fueron transformadas en variables dummy para la segunda parte del proyecto.
En la primera parte del proyecto además de realizar los procedimientos previamente mencionados, se hizo un análisis univariado, bivariado y multivariado,
enfocándonos principalmente en diferenciar las características de aquellos que son más propensos a “defaultear” un préstamo y aquellos que no.
Como se mencionó, las variables principales son educación, ingresos, cantidad de dinero solicitado, situación civil, vivienda y ciudad, etc.

En la segunda parte del proyecto, se utilizaron diferentes modelos para la predicción de la variable target, en este caso fraude o no fraude.
Nuestra métrica de interés es el recall de la clase fraude, ya que queremos maximizar la cantidad de predicción de fraudes (falsos positivos) y a la vez reducir los falsos negativos,
es decir la predicción de "no fraude" cuando si lo es. Los modelos utilizados fueron: Regresión Logistica, Decision Tree, Random Forest y dos modelos de boosting: CatBoost y LightBoost.
Uno de los problemas principales de la base de datos es que presenta un desbalanceo de clase, un 95% de los valores son “no fraude” y tan solo un 5% pertenece a fraude,
al momento de utilizar los modelos, es necesario balancearla, ya sea por parametrización, oversampling, subsampling o la combinación de estos dos últimos,
se optó por utilizar la combinación (SMOTE) Se utilizaron algunas herramientas para la optimización de los modelos como; Stratifield K-Folds, GridSearchCV, RandomizedSearchCV.
Aunque también se pudieron haber utilizado otras como: Reducción de dimensionalidad, Optimización bayesiana, la cual esta última no se utilizó por el uso computacional requerido.
