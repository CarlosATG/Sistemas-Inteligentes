Proyecto de Algoritmos Avanzados

Este repositorio alberga una colección de implementaciones de algoritmos avanzados aplicados a una variedad de problemas clásicos en el campo de la optimización y la computación. A continuación se presenta una descripción más detallada de cada problema y las técnicas específicas que se utilizaron para resolverlos.
1. Sudoku

Problema: El Sudoku es un popular rompecabezas que consiste en llenar una cuadrícula 9×99×9 de manera que cada fila, cada columna y cada subcuadrícula 3×33×3 contenga los números del 1 al 9 sin repetirse. El reto es encontrar una solución válida partiendo de un tablero incompleto que ya tiene algunos números predefinidos.

Solución: Para resolver este problema, se ha implementado un enfoque híbrido. Primero, se utilizó un algoritmo de Recocido Simulado que iterativamente modifica el tablero, intercambiando números para minimizar el número de conflictos en filas, columnas y subcuadrículas. Este método es ideal para escapar de mínimos locales debido a su capacidad de aceptar soluciones subóptimas en las primeras etapas. Luego, se refinó la solución utilizando un Algoritmo Genético, que simula el proceso de evolución natural. El algoritmo combina y muta diferentes soluciones parciales para mejorar gradualmente hasta encontrar un tablero completamente resuelto.

2. Cuadrados Mágicos

Problema: Un cuadrado mágico es una disposición de números en una cuadrícula de n×nn×n donde la suma de los números en cada fila, columna y diagonal principal es la misma. El objetivo es construir tal cuadrado mágico, un problema que se complica exponencialmente con el tamaño del cuadrado.

Solución: Para abordar este desafío, se utilizó el Recocido Simulado, un algoritmo heurístico que imita el proceso de enfriamiento de metales. Comenzando con un cuadrado inicial que no es mágico, el algoritmo realiza pequeños cambios, como intercambiar dos números, y acepta estos cambios si mejoran la configuración o si, dado un cierto grado de "temperatura", no la empeoran mucho. A medida que la temperatura baja, el sistema se estabiliza, conduciendo a una solución donde las sumas de las filas, columnas y diagonales convergen a la constante mágica.

3. Asignación de Edificios

Problema: Este problema involucra la asignación de cuatro edificios a cuatro sitios de tal manera que se minimicen los costos asociados. Los costos dependen tanto de las distancias entre los sitios como del número de conexiones entre los edificios. Este problema de asignación cuadrática es representativo de muchas situaciones en logística y planificación urbana.

Solución: Se empleó el Recocido Simulado para explorar el espacio de posibles asignaciones y buscar una configuración que minimice el costo total. A través de iteraciones sucesivas, el algoritmo ajusta la asignación, evaluando cada cambio en términos del costo resultante y utilizando la probabilidad de aceptación para explorar posibles soluciones mejores, incluso si requieren un paso a través de configuraciones subóptimas.

4. Problema de las 8 Reinas

Problema: El problema de las 8 reinas es un clásico en el que se deben colocar 8 reinas en un tablero de ajedrez 8×88×8 de manera que ninguna pueda atacar a otra. Las reinas pueden atacar a cualquier otra pieza que esté en la misma fila, columna o diagonal.

Solución: Para resolver este problema, se utilizó un algoritmo de Recocido Simulado. Se empieza con una configuración aleatoria de las 8 reinas y, en cada iteración, se genera una nueva configuración moviendo una reina a una nueva posición. El algoritmo evalúa cuántos conflictos (ataques entre reinas) existen en la nueva configuración y decide si acepta la nueva disposición basada en si reduce el número de conflictos o si la probabilidad de aceptación lo permite. Este enfoque permite encontrar una configuración en la que ninguna reina pueda atacar a otra, resolviendo así el problema.

5. Función de Shubert

Problema: La función de Shubert es una función multimodal compleja que tiene múltiples máximos y mínimos locales, lo que la convierte en un desafío interesante para los algoritmos de optimización. La función se define sobre dos variables y exhibe un comportamiento altamente oscilatorio.

Solución: Para identificar los máximos y mínimos locales de esta función, se empleó el Hill Climbing. Este algoritmo comienza en un punto inicial y explora los puntos vecinos para encontrar mejoras. Si encuentra un vecino con un valor superior (en el caso de buscar un máximo) o inferior (en el caso de buscar un mínimo), se mueve a ese punto y repite el proceso. La implementación genera una gráfica de la función en 2D y marca los máximos y mínimos locales encontrados, proporcionando una visualización clara de los resultados del algoritmo.

6. Multiplicación de Karatsuba

Problema: La multiplicación de grandes números enteros es un problema fundamental en la teoría de la computación. El algoritmo de multiplicación tradicional tiene una complejidad de tiempo de O(n2)O(n2), lo que se vuelve ineficiente para números muy grandes.

Solución: El Algoritmo de Karatsuba es una técnica recursiva que mejora la eficiencia de la multiplicación al reducir el número de operaciones necesarias. En lugar de realizar cuatro multiplicaciones de números más pequeños, como haría el enfoque tradicional, Karatsuba lo hace con solo tres multiplicaciones, aprovechando la división del problema en subproblemas más pequeños. Esta implementación es capaz de manejar eficientemente la multiplicación de números grandes, como 1024×10241024×1024, demostrando la efectividad del método en comparación con la multiplicación directa.
