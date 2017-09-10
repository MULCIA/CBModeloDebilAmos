# Portada

En esta presentación se va a abordar la resolución del problema de la generación de permutaciones desde el punto de vista de la computación molecular y, también, el problema del camino hamiltoniano sobre un grafo.

Se explica en este orden debido a que el diseño del programa es muy similar, y se necesita el modelado del primer problema para resolver el segundo problema.

Antes de entrar a hablar sobre dichos problemas, se va a hacer una breve introducción a la computación molecular.

# ADN

En pantalla se muestra una doble hélice de ADN. Esta doble hélice la forman dos cadenas simples de ADN unida a través de las bases por puentes de hidrógeno. Que pueden ser dos o tres puentes según cuales sean las bases que se unen, y que dan más fuerza a ese enlace.

Cada cadenas simple tiene una polaridad que viene determinada por según que grupo quedan sin unir en los extremos. Esto hace que la doble hélice se forme con dos cadenas simples de forma antiparalela o, con polaridades opuestas.

Para terminar, las cadenas simples las forman nucleotidos que son una base nitrogenada, que puede ser A,C,G,T. Y esta está unida a un azúcar de cinco átomos de carbono a través del primer átomo. Los dos grupos: fosfodiester e hidrógeno, son los que se muestran respectivamente unidos al azúcar a través del átomo quinto y átomo tercero.

# Computación molecular

Explicado en qué consiste el ADN, que es el sustrato que permitirá hacer computo, pasamos a describir en qué consiste este tipo de computación.

(Ver diapositiva)

# Operaciones con moléculas de ADN

Aquí se muestran algunos ejemplos de operaciones.

(Ver diapositiva)

# Modelo débil de Amos

Aquí se describe brevemente en qué consiste el modelo débil de Amos.

Se parte con un tubo de ensayo que contiene un multiconjunto finito de cadenas con alfabeto que se muestra, correspondiente con las bases de los nucleotidos: Adenina, Guanina, Timina y Citosina.

Sobre ese tubo se ejecutan una serie de operaciones, llamadas primitivas:

* La operación quitar consiste en dado un tubo y un número finito de de cadenas, se devuelve un tubo eliminan todas aquellas cadenas que contengan, al menos, una ocurrencia de alguna de dichas cadenas.
* Se devuelven desde 1 hasta n copias del tubo principal.
* Dados una serie de tubos, se devuelve un único tubo que contiene la union de todos los tubos recibidos como multiconjuntos.
* Dado un tubo, se selecciona aleatoriamente un elemento en caso de que el tubo no esté vacío.

# Problema de la generación de permutaciones

En primer lugar, se va a mostrar como resolver el problema de la generación de permutaciones. En la imagen, se muestra una definición gráfica del problema. Consiste en una aplicación biyectiva entre un conjunto de números consigo mismo.

Por tanto, necesitamos generar todas las posibles combinaciones.

# Diseño del programa molecular

Se necesita un alfabeto, una representación las moléculas de ADN que se encuentran en el tubo.

También, se necesita un tubo inicial, o de entrada, que contiene moléculas de ADN que modelan todas las posibles sucesiones.

El algoritmo es el que se muestra en pantalla, y consiste en aplicar una serie de filtrados:

* Un primer filtro para todas las posiciones se devuelven todas aquellas codificaciones, tal que, el resto de posiciones no contengan el valor contenido en la primera posiciones.
* Un segundo filtro, a partir del anterior, que hace lo mismo pero comprobando que no es igual ni para la primera ni para la segunda posición.

# Previo a la verificación formal

Se reescribe el algoritmo de modo que se pueda etiquetar cada tubo en el algoritmo. Se representa con una fórmula matemática.

Se busca probar la correción y la completitud, es decir, para cada caso se busca probar la invarianza, mediante un teorema, y la correción, mediante un corolario. De este modo, la fórmula cumplirá en cada caso que es verdadera al comenzar el bucle, que es invariante y que satisface la propiedad.

# Verificación formal

(Ver diapositiva)

# Problema del camino hamiltoniano

Se busca un camino simple que recubra todo el grafo.

# Diseño del programa molecular

Este programa se modela igual que el anterior. Aquí cambia el algoritmo que se aplican diferentes filtrados:

* Se seleccionan las moleculas del tubo, tal que, el segundo elemento sea un camino del grafo.
* De estas, se seleccionan aquellas tal que el tercer elemento es también un camino del grafo.

# Verificación formal

(Ver diapositiva)
