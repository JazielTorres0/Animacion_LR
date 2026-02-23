____________________________________Introducción____________________________________
Este documento describe el funcionamiento de un ejemplo en HTML y JavaScript que simula el análisis sintáctico LR(1). La simulación se basa en una tabla LR(1) y
muestra paso a paso el comportamiento de la pila, la entrada y las acciones realizadas durante el análisis.


____________________________________Estructura del Código___________________________
El código HTML está dividido en las siguientes secciones principales:

    1. Tablas LR(1): Definen los estados y transiciones de la gramática a analizar.
    2. Tablas de Animación: Muestran dinámicamente los pasos de la simulación.
    3. Botones de Control: Permiten iniciar la simulación para cada ejemplo.
    4. Script en JavaScript: Contiene la lógica de la animación, similar a la estructura
modular del analizador léxico en Python.

____________________________________Funcionamiento____________________________________
1. Definición de pasos (steps1 y steps2): Cada paso está representado como un
objeto con tres atributos: pila, entrada y salida. Esto equivale a las listas de pasos utilizadas en la versión en Python.

2. Función simulateParsing: Esta función recibe la lista de pasos y el ID de la tabla en la que se mostrará la animación. De manera cíclica, recorre los pasos y los
inserta en la tabla, simulando el proceso del análisis LR(1).

3. Ejecución: Cada botón invoca la función simulateParsing con el conjunto de pasos correspondiente, mostrando de forma visual la evolución del análisis.

____________________________________Ejemplo de Uso____________________________________
Entrada (Ejemplo 1): a+b$
Pasos de la simulación:
Pila: $0 | Entrada: a+b$ | Salida: d2
Pila: $0a2 | Entrada: +b$ | Salida: d3
Pila: $0a2+3 | Entrada: b$ | Salida: d4
Pila: $0a2+3b4 | Entrada: $ | Salida: r1 E→id+id
Pila: $0E1 | Entrada: $ | Salida: acept

Entrada (Ejemplo 2): a$
Pasos de la simulación:
Pila: $0 | Entrada: a$ | Salida: d2
Pila: $0a2 | Entrada: $ | Salida: r1 E→id
Pila: $0E1 | Entrada: $ | Salida: aceptación

____________________________________Conclusión____________________________________
El ejemplo en HTML y JavaScript permite visualizar de manera clara el
funcionamiento del análisis LR(1). Su estructura modular refleja la misma filosofía
del analizador léxico en Python, facilitando su comprensión y adaptación para
proyectos educativos o de compiladores.
