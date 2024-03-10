# Y más ...

La __visión artificial__ es una de las especialidades del __aprendizaje automático__ (_machine learning_). Dentro de la visión artificial la identificación de imágenes resuelta con las redes convoluciones es un buen ejemplo para introducir el __aprendizaje profundo__ (_deep learning__). Pero es uno de los ejemplos más sencillos de abordar y aunque útil no resuelve problemas más generales.

Una vez prendida la curiosidad, lo recomendable es seguir profundizando en las dos siguientes propuestas de la visión artificial:
- La __segmentación__ de imágenes supervisada con redes neuronales.
- La __instanciación__ de imágenes.

La __segmentación__ supervisada con redes neuronales fue propuesta por {cite:p}`ronneberger2015u` sustituyendo la red densa o __capa fully connected__ por un nuevo conjunto de capas convolucionales. De forma que se tienen dos bloques, primero un __Encoder__ seguido de un __Decoder__. 


<img src="images/RedFullyConvolutional.png" alt="RedFullyConvolutional" width="600px" align="center">


La __instanciación__ combina la segmentación con la detección de imagenes, resultando un tratamiento de mayor complejidad. Primero segmenta y marcos de interés, identificando cada uno de ellos

<img src="images/Segmen_COCO.png" alt="SegmenCOCO" width="700px" align="center">


```{note}

Mis agradecimientos por su contribución y apoyo a Carlos García-Guitérrez, José Ángel Capitán, Juan Carlos Nuño, Belén Diezma y Pilar Barreiro.
```


