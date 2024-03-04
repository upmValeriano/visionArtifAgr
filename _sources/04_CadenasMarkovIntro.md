<!-- #region -->
# Cadenas de Markov

En este capítulo veremos como modelizar secuencias biológicas mediante [modelos de Markov](https://en.wikipedia.org/wiki/Markov_model). En particular estamos interesados en predecir la estructura secundaria de proteínas a través de un [modelo oculto de Markov](https://en.wikipedia.org/wiki/Hidden_Markov_model). Este capítulo está basado en el trabajo {cite}`Asai1993`.


## Práctica

* En la primera práctica veremos cadenas de Markov como modelos de secuencias. 
* En la segunda buscaremos la predicción de estructuras secundarias en proteínas.

### Objetivos

1. Parametrizar __cadenas de Markov__ mediante secuencias genéticas.
2. Analizar e interpretar las distribuciones de equilibrio.
3. Calcular la secuencia más probable en una __cadena de Markov__.
4. Utilizar secuencias de aminoácidos con estructuras secundarias __anotadas__ para parametrizar un __modelo de Markov oculto__.
5. Predecir estructuras secundarias a partir del conjunto de entrenamiento.

## Datos

En este capítulo usaremos el fichero de datos `prots-L30.txt` que puedes encontrar en Moodle y en <a href="./data/prots-L30.txt"> este enlace</a>.



<!-- #endregion -->
