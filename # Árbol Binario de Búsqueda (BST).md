# Árbol Binario de Búsqueda (BST)

## Descripción

Proyecto desarrollado en Java utilizando Maven. Consiste en la implementación manual de un Árbol Binario de Búsqueda (BST) sin utilizar estructuras de datos de `java.util`.

Además de las operaciones básicas del árbol, se implementaron cinco problemas obligatorios y cuatro ejercicios extra relacionados con recorridos, validaciones y análisis de árboles binarios.

---

# Requisitos

* Java JDK 11 o superior
* Apache Maven 3.8 o superior
* Eclipse IDE (opcional)

---

# Compilación

Desde la carpeta raíz del proyecto:

```bash
mvn clean compile
```

---

# Ejecución

```bash
mvn exec:java -Dexec.mainClass="umg.edu.progra.arboles.Principal"
```

---

# Estructura del árbol de prueba

El programa inserta los siguientes valores:

```text
50, 30, 70, 20, 40, 60, 80, 10
```

Generando el siguiente BST:

```text
              50
             /  \
           30    70
          / \   / \
        20 40 60 80
       /
      10
```

---

# Problema 1 - contarNodos()

## Descripción

Cuenta la cantidad total de nodos del árbol utilizando recursividad sin utilizar el atributo `tamanio`.

## Ejemplo

### Entrada

Árbol de prueba.

### Salida

```text
Tamanio: 8
Nodos (recursivo): 8
```

---

# Problema 2 - esBalanceado()

## Descripción

Verifica si el árbol está balanceado.

Un árbol se considera balanceado cuando para cada nodo la diferencia de alturas entre los subárboles izquierdo y derecho es menor o igual a 1.

## Ejemplo verdadero

```text
Balanceado: true
```

## Ejemplo falso

```text
===== PRUEBA ARBOL DESBALANCEADO =====
Balanceado: false
```

---

# Problema 3 - esBSTValido()

## Descripción

Verifica que todos los nodos cumplan la propiedad de Árbol Binario de Búsqueda.

## Ejemplo verdadero

```text
BST valido: true
```

## Ejemplo falso

```text
===== PRUEBA BST INVALIDO =====
BST valido: false
```

---

# Problema 4 - ancestroComunMasBajo()

## Descripción

Obtiene el ancestro común más bajo (Lowest Common Ancestor - LCA) de dos valores utilizando las propiedades del BST.

## Ejemplos

```text
LCA(10,40): 30
LCA(10,80): 50
LCA(60,80): 70
```

## Manejo de errores

Si alguno de los valores no existe en el árbol:

```text
===== PRUEBA EXCEPCION LCA =====
Excepcion capturada: Uno o ambos valores no existen en el arbol
```

---

# Problema 5 - invertir()

## Descripción

Invierte el árbol creando su imagen espejo.

## Antes

```text
InOrden antes:
10 20 30 40 50 60 70 80
```

## Después

```text
InOrden despues:
80 70 60 50 40 30 20 10
```

---

# Ejercicios Extra

## E1 - kEsimoMenor()

Obtiene el k-ésimo valor más pequeño mediante recorrido InOrden.

### Ejemplo

```text
1er menor: 10
3er menor: 30
8vo menor: 80
```

---

## E2 - imprimirRangoOrdenado()

Imprime los valores comprendidos dentro de un rango dado.

### Ejemplo

```text
Rango [25,70]: 30 40 50 60 70
Rango [40,80]: 40 50 60 70 80
```

---

## E3 - diametro()

Calcula el diámetro del árbol, es decir, el camino más largo entre dos nodos.

### Ejemplo

```text
Diametro: 5
```

---

## E4 - Construcción desde args[]

Permite construir un BST utilizando valores enviados como argumentos de ejecución.

### Ejemplo

```bash
mvn exec:java -Dexec.mainClass="umg.edu.progra.arboles.Principal" -Dexec.args="50 30 70 20 40 60 80 10"
```

---

# Restricciones Cumplidas

* No se utilizó `java.util`.
* No se utilizaron librerías externas.
* Se implementaron estructuras auxiliares manualmente.
* Toda la lógica fue desarrollada dentro del paquete `umg.edu.progra.arboles`.
* Todos los métodos fueron probados desde la clase `Principal`.

