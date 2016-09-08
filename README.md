# TextMining

Este es el código utilizado para resolver el problema Hispatweet planteado como práctica de la asignatura del master de Big Data de la UPV.

Los ficheros que se pueden encontrar son los python notebook para ejecutar el codigo así como los ficheros que se van generando en la ejecución de los mismos. Tan bien se ha generado una versión del notebook en html por si no se dispone de software para verlos y se quiere ver el código.

El problema se ha separado en dos uno para distinguir el país del autor y otro para distinguir el sexo, los ficheros para cada uno de los problemas son:

## Detectar país.

1. TextMining.ipynb. Contiene el código para obtener la bolsa de palabras a utilizar así como los ficheros de vectores de características de training y test. Los ficheros generados son los siguientes:
  * bolsadepalabras.txt. Como su nombre indica contiene la bolsa de palabras generada.
  * trainingdata.txt. Contiene los vectores de caracteristicas obtenidos de los datos de training.
  * testdata.txt. Contiene los vectores de caracteristicas obtenidos de los datos de test
2. ModelPais.ipynb. Contiene el código que a partir de los ficheros trainingdata.txt y testdata.txt, entrena un modelo y lo valida con los datos de test.


## Detectar sexo.

3. TextMiningSexProfiling.ipynb. Contiene e código para generar un vector de caracteristicas de cada autor dependiendo de el tipo de palabras que usan, se calculan contadores del número de determinantes, pronombres, etc. Para más detalles, leer la memoria de la practica. Los ficheros generados son:
   * sextrainingdata.txt. 
   * sextestdata.txt
4. SexProfilingWords.ipynb. Contiene el código para generar una bolsa de palabras con las palabras usadas por un sexo y no por otro y algunas de las palabras más usadas en general y generar vectores de caracteristicas. Estos vectores de caracterisiticas se fusionan con los vectores de características almacenados en los ficheros sextrainingdata.txt y sextestdata.txt. Los ficheros generados son:
    * sexwordtrainingdata.txt. Contiene los vectores de caracteristicas de los datos de training para la bolsa de palabras generada.
    * sexwordtestdata.txt. Contiene los vectores de caracteristicas de los datos de test para la bolsa de palabras generada.
    * sexmergetrainingdata.txt. Contiene los vectores de caracteristicas resultado de fusionar los de sextrainingdata.txt y sexwordtrainingdata.txt.
    * sexmergetestdata.txt. Contiene los vectores de caracteristicas resultado de fusionar los de sextestdata.txt y sexwordtestdata.txt.
    
5. ModelSex.ipnb. Contiene el código que a partir de los vectores de caracteristicas generados entrena un modelo y lo valida con los datos de test.
