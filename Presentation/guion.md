Computación molecular sin memoria basada en ADN
===

En esta presentación se va a explicar como diseñar un programa molecular para resolver los problemas de la generación de permutaciones y, también, el problema del camino hamiltoniano.

El orden de presentación de presentación los problemas es importante, ya que, el problema del camino hamiltoniano se va a presentar como un problema de generación de permutaciones.

Al principio, se va a introduccir brevemente en que consiste la programación molecular.

---

# ADN

En la presentación se puede ver lo que sería una doble hélice de ADN. Se compone de dos cadenas simples, las cuales tienen una determinada polaridad, que viene dado por los enlaces que quedan sin utilizar.

En este caso, las Bases están unidas por puentes de hidrógeno, que serán de dos o tres puentes y, por tanto, más resistentes, dependiendo del tipo de base.

Las bases pueden ser 4: A,C,G,T. La A se une con la T y la C con la G. 

Cada base

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
```
PARA j = 1 hasta n - 1 HACER:
    copiar(T0,{T1,...,Tn})
    PARA i = 1 hasta n HACER:
        quitar(Ti, {})
    union({T1,...,Tn}, T0)
DEVOLVER T0
```

---

# Verificación formal

---

# Problema del camino hamiltoniano

<div style="text-align:center"><img width="400" height="400" src="./images/hamiltoniano.png"/></div>

---

# Diseño molecular

- Alfabeto `(pi,cj)` para todo `i,j` entre `[1,n]`.
- Dado un tubo de entrada `T0` que contiene todas las posibles sucesiones:
```
PARA i = 1 hasta n - 1 HACER:
    T0 = quitar(T0, {})
DEVOLVER seleccionar(T0)
```

---

# Verificación formal

---

# Gracias

<div style="text-align:center"><img width="300" height="300" src="http://ahoragetafe.es/wp-content/uploads/2016/11/descarga-1.jpg" /></div>

---