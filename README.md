## Introducción
Los conjuntos de datos utilizados en este proyecto han sido el de precios de piso (de ahora en adelante dfp), ya que es el conjunto base, y el de la contaminación acústica (de ahora en adelante, dfc), ya que en grandes metrópolis como Barcelona, la contaminación acústica es un factor a tener en cuenta a la hora de comprar una vivienda.

## Depuración de datos
La depuración de los datos de cada dataset se puede resumir en los siguientes puntos:
    
* `Reorganización de los datos`: se ha reorganizado el dataset con tal de hacerlo más legible, accesible y, lo más importante, facil de juntar con el otro dataset. Además, este proceso ha eliminado mucha redundancia de datos, lo cual siempre es positivo.

* `Tratamiento de NaNs`: En dfp el tratamiento dado ha sido escaso, pues solo 3 filas contenian NaNs y, por desgracia, en dos de ellas la proporción era tan grande que no era viable imputarlos. En el otro caso, sí que se han imputado los datos, haciendo uso de la media de los valores correspondientes al mismo atriuto en otros momentos del año

Sobre dfc, no ha sido necesario tomar ninguna medida, pues no contenia NaNs.

* `Escalado`: Como es bien sabido, procesos como el PCA requieren de estandarizado previo a su ejecución, por lo que se ha aplicado a ambos datasets. Se ha optado por un escalado estándar, pues es el más común y el que mejores resultados suele dar.

* `Unión de los sets de Datos`: Proceso sencillo, pues la reorganización de los datos ha facilitado mucho el proceso. Se ha optado por unirlos por distrito y barrio, pues son los atributos que tienen en común. 

## Resultados

Los resultados son que con tan solo 3 dimensiones se puede explicar más del 80% de la varianza total del dataset unión de dfp y dfc. Esto es muy positivo, pues se ha conseguido reducir el número de dimensiones de 35 a 3. Además, las dimensiones parecen tener una interpretación clara, al menos a un nivel básico, lo que facilita su interpretación.

## Conclusiones

Podemos observar claramente que la primera y tercera dimensión explican principalmente la contaminación acústica, mientras que la segunda explica principalmente el precio. Este es un resultado muy interesante, ya que muestra que el precio no está (fuertemente) relacionado con la contaminación acústica, sino con otros factores que caen fuera del alcance de este análisis.

Desde la dimensión 3, podemos observar que los niveles de contaminación acústica total están fuertemente relacionados con los niveles de contaminación acústica producida principalmente por el tráfico. Este es un resultado muy interesante, ya que muestra que la contaminación acústica producida por el tráfico es la principal fuente de contaminación acústica en Barcelona, lo cual es un hecho muy importante a tener en cuenta al diseñar nuevas áreas urbanas.

En cuanto a otros tipos de contaminación acústica, podemos observar que no están fuertemente relacionados con la contaminación acústica total, lo que significa que no son una fuente importante de contaminación acústica en Barcelona. Aun así, eso no implica que no sean importantes, ya que la contaminación acustica total no es la única métrica válida para medir la gravedad de la contaminación acústica.

Sin embargo, se podría extraer más información si tuviéramos conocimiento profesional sobre el tema. Por ejemplo, el significado de los diferentes tipos de contaminación acústica, cómo se miden, etc. Todo esto se deja para futuros análisis.