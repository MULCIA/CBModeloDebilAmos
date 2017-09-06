Computación molecular sin memoria basada en ADN
===

#####  Problemas de generación de permutaciones y camino hamiltoniano

###### Sergio Rodríguez Calvo, Septiembre 2017. 
###### Computación Bioinspirada (MULCIA), Universidad de Sevilla.

---

# ADN

<div style="text-align:center"><img width="500" height="500" src="./images/molecula_adn.png"/></div>

---

# Computación Molecular

- Tubo de ensayo contiene una solución con cadenas simples de ADN (oligos).
- Automatización de procesos sobre los tubos que realizan operaciones abstractas, tales como, medir, sumar, etc.
- Necesario un modelado y representación del problema adecuado para este tipo de computación.

---

# Operaciones con moléculas de ADN

Algunos ejemplos de operaciones son:

- Desnaturalización: separar doble hebra calentando solución hasta un rango de 85ºC - 95ºC.
- Extracción: extraer de un tubo todas las moléculas que contienen una determinada subcadena, utilizando el método de las sondas metálicas.
- Cortar cadenas: uso de enzimas endonucleasas que cortan cadenas (simples o dobles) por cualquier sitio.

---

# Modelo débil de Amos

- Tubo de ensayo con un multiconjunto finito de cadenas con alfabeto `{A,C,G,T}`.
- Operaciones en el modelo débil de Amos (primitivas) son:
  - `Quitar(T,{s1,...,sn})`.
  - `Copiar(T,{T1,...,Tn})`.
  - `Unión({T1,...,Tn})`.
  - `Selección(T)`.

---

# Problema de la generación de permutaciones

- Permutación: <div style="text-align:center"><img width="150" height="150" src="./images/permutaciones.jpeg"/></div>
- Problema: _dado un numero natural n mayor o igual que 2, generar todas las permutaciones de orden n_.

---

# Diseño molecular

- Alfabeto `(pi,cj)` para todo `i,j` entre `[1,n]`.
- Dado un tubo de entrada `T0` que contiene todas las posibles sucesiones:

![](./images/prob1_1.png)

---

# Previo a la verificación formal

- Buscar una fórmula que cumpla (p. corrección y completitud):
    - Fórmula es verdadera antes de comenzar el bucle.
    - Fórmula es invariante en dicho bucle (por inducción débil).
- Reetiquetado.
- Corrección del programa (Teorema + Corolario).
- Completitud del programa (Teorema + Corolario).


---

# Verificación formal

- Se reescribe el código para enumerar los tubos:

![](./images/prob1_2.png)

* _Ver documento_.

---

# Problema del camino hamiltoniano

<div style="text-align:center"><img width="400" height="400" src="./images/hamiltoniano.png"/></div>

---

# Diseño molecular

- Alfabeto `(pi,cj)` para todo `i,j` entre `[1,n]`.
- Dado un tubo de entrada `T0` que contiene todas las posibles sucesiones:

![](./images/prob2_1.png)

---

# Verificación formal

- Se reescribe el código para enumerar los tubos:

![](./images/prob2_2.png)

* _Ver documento_.

---

# Gracias

<div style="text-align:center"><img width="300" height="300" src="http://ahoragetafe.es/wp-content/uploads/2016/11/descarga-1.jpg" /></div>

---