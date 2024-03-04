# Mapas Autoorganizativos

En este capítulo se estudian los [Mapas Autoorganizativos](https://en.wikipedia.org/wiki/Self-organizing_map) de [Teuvo Kohonen](https://en.wikipedia.org/wiki/Teuvo_Kohonen). En inglés _Self Organizing Map (SOM)_.

## Motivación

Existen, cada vez más y en particular en las ciencias _ómicas_, grandes bases de datos donde no hay una variable respuesta. 

Podemos usar la idea de espacio vectorial para conceptualizar estas bases de datos. Cada instancia es un punto (vector) en $\mathbb{R}^N$, donde $N$ es el número de características/atributos/_features_ de cada instancia.

En muchos casos sucede que datos _cercanos_ en este espacio representan _actividad_/información similar
*  _nubes_ de puntos.

La interpretación de los datos es más lenta que su generación. En muchos casos los métodos convencionales de estadística multivariante no funcionan bien. Algunas causas pueden ser:
* ratio _signal-to-noise_ bajo
* _missing data_
* _small sample sizes relative to huge gene volumes_

Los datos no pueden ser descritos de manera satisfactoria con los parámetros estadísiticos de bajo orden (media, varianza), las distribuciones no son Gaussianas, los estadísticos no son estacionarios. Las relaciones funcionales no son lineales en la mayor parte.

> Son necesarios métodos adaptativos o redes-neuronales, que sean eficientes computacionalmente.

### Inspección visual

Visualizar los datos es un paso crucial para descubrir relaciones entre ellos (e.g. genes y muestras)
* [data mining](https://en.wikipedia.org/wiki/Data_mining)
* [análisis exploratorio de los datos](https://en.wikipedia.org/wiki/Exploratory_data_analysis)

Se buscan algorimos de 
* _clustering_
* proyección
* visualización 
que preserven la [__topología__](https://es.wikipedia.org/wiki/Topolog%C3%ADa) (forma y densidad) de los datos multidimensionales.

__Objetivo:__ explorar la estructura geométrica de una representación _bajo_-dimensional que conserve la topología para descubrir relaciones/procesos/información (biológicos) significativas

Estamos _casi_ limitados por visualizaciones tridimensionales: es necesario [reducir la dimensión](https://en.wikipedia.org/wiki/Dimensionality_reduction)

### $K$-means

Problemas:
   * Elegir $k$
   * _Outliers_
   * Representación?

### El SOM

Los __Self-Organising Maps__ (SOMs) son un algoritmo de aprendizaje no supervisado que permite visualizar datos en _altas_ dimensiones mediante representaciones en dimensiones menor (típicamente dim=2). Este algoritmo ha resultado ser adecuado para el análisis de datos multidimensionales por su habilidad para preservar la topología de los mismos.

El SOM produce, usualmente, un grid hexagonal en dos dimensiones de los nodos del mapa. Cada nodo del mapa tiene asociado un vector _prototipo_ del espacio mayor $\mathbb{R}^N$ donde viven los datos. A esta disposición se la conoce como _codebook matrix_.

```{figure} ./images/som_esquema.png
---
scale: 50%
align: left
---
Nodos y vectores prototipo
```
```{figure} ./images/SOM_R_1.jpg
---
scale: 70%
align: right
---
Ejemplo de _mapa- SOM
```

El resultado del algoritmo resulta adecuado para la inspección visual del científico.

En particular, usando datos genómicos, el SOM produce un mapa que:
* genes con patrones de actividad similares (vectores de actividad) son asociados con el mismo nodo o nodos cercanos en el mapa
* la distribución de genes en el mapa bidimensional es semejante a la distribución en el espacio de mayor dimensión

## Aplicaciones en biotecnología

El SOM se utiliza con mucha frecuencia en biotecnología. En la sección {ref}`som:aplicacionesbiotecnologia` pueden verse algunas.

## Bibliografía genérica

+ {cite}`Johnsson2012`
+ {cite}`OjaKaski1999`
+ {cite}`Kohonen2000`

## Práctica

* En la primera práctica veremos cómo implementar el algoritmo SOM en una dimensión
* Veremos cómo realizar el _clustering_ de regiones vinícolas
* Aplicaremos el SOM para el estudio de comunidades microbianas

### Objetivos

1. Entender los fundamentos del SOM en un caso unidimensional
2. Aplicación los paquetes SOM para agrupar los datos `wine`
3. Visualización los _clusters_
4. Aplicación al estudio de la formación de comunidades bacterianas

## Datos

En este capítulo utilizaremos los siguientes datos:
 * `iris`
 * datos del censo irlandés, año 2011, <a href="https://github.com/shanealynn/Kohonen-Self-organising-maps-in-R/"> enlace GIT</a> y fichero `dataIrelandPopulationSOM.csv` que podéis encontrar en Moodle y en <a href="./data/dataIrelandPopulationSOM.csv"> este enlace </a>.
 * los datos de las características de unos vinos pertenecientes a tres bodegas italianas (fichero de datos `wines` incorporado a R o `wine.csv` que se puede encontrar en Moodle y en <a href="./data/wine.csv"> este enlace </a>.
 * datos de comunidades microbianas; fichero `community_structure.csv` que puedes encontrar en Moodle y en <a href="./data/community_structure.csv"> este enlace</a>.

