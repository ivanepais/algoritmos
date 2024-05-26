# algoritmos


|| Algoritmos


	1. Definición de algoritmo.

    2 Características de un buen algoritmo: 

    	(finitud, claridad, entrada/salida, efectividad).


    Algoritmo: 	

    	Es una secuencia bien definida de pasos o instrucciones que se utilizan para resolver un problema o realizar una tarea específica. 

    	Son fundamentales en la programación y en la informática en general, ya que proporcionan una guía sistemática para la resolución de problemas.


    Definición: 

    	Un algoritmo es un conjunto finito de instrucciones bien definidas y no ambiguas que se deben seguir para llevar a cabo una tarea o resolver un problema.


	Propósito: 

		Los algoritmos se utilizan para automatizar la solución de problemas, permitiendo a las computadoras realizar tareas complejas de manera eficiente y efectiva


	Propiedades:

		Finito: 

			Un algoritmo debe tener un número finito de pasos. 

			Debe terminar en algún momento.


		Definido: 

			Cada paso del algoritmo debe estar claramente definido y no debe haber ambigüedad en las instrucciones.


		Entrada: 

			Un algoritmo puede tener cero o más entradas, que son los datos que se suministran al algoritmo para que procese.


		Salida: 

			Un algoritmo debe producir al menos una salida, que es el resultado del procesamiento de las entradas.


		Efectividad: 

			Las operaciones del algoritmo deben ser lo suficientemente básicas para que puedan ser realizadas, en principio, de manera exacta y en un tiempo finito.


	Tipos de Algoritmos:

    	Algoritmos de Ordenación: 

    		Se utilizan para ordenar elementos en una secuencia (por ejemplo, QuickSort, MergeSort).


   		Algoritmos de Búsqueda: 

   			Se utilizan para encontrar un elemento específico dentro de una estructura de datos (por ejemplo, Búsqueda Binaria).


   		Algoritmos de Recorrido: 

   			Se utilizan para recorrer o visitar todos los nodos en una estructura de datos (por ejemplo, Depth-First Search, Breadth-First Search).


	    Algoritmos de Optimización: 

	    	Se utilizan para encontrar la mejor solución entre muchas posibles (por ejemplo, Algoritmo de Dijkstra para encontrar el camino más corto).


	Ejemplo: 

		Algoritmo básico para encontrar el número máximo en una lista de número: 

		```python

		def encontrar_maximo(lista):
		    maximo = lista[0]
		    for numero in lista:
		        if numero > maximo:
		            maximo = numero
		    return maximo

		```

		Entrada: 

			Una lista de números.
    
    	Proceso: 

    		Comenzar con el primer número como el máximo provisional y luego iterar a través de la lista, actualizando el máximo si se encuentra un número mayor.

    	Salida: 

    		El número máximo en la lista.


    Importancia de los Algoritmos:

    	Eficiencia: 

    		Los algoritmos permiten resolver problemas de manera eficiente, utilizando los recursos de la computadora (como tiempo y memoria) de manera óptima.


    	Escalabilidad: 

    		Un buen algoritmo puede manejar grandes cantidades de datos de manera efectiva, algo crucial en aplicaciones del mundo real.


    	Automatización: 

    		Los algoritmos son esenciales para la automatización de tareas, permitiendo que las computadoras realicen trabajos repetitivos y complejos sin intervención humana.



|| Ejemplos de Algoritmos Básicos


	Suma: 
	
		1. Definir los conceptos del problema: 

			Ej. Sumar dos números dados y devolver el resultado.


			Pseudocódigo: 

				```
				Inicio
				    Leer número1
				    Leer número2
				    Sumar número1 y número2
				    Mostrar el resultado
				Fin

				```

		2. Implementar la solución en un lenguaje de programación: 

			```python

			def sumar_numeros(numero1, numero2):
			    resultado = numero1 + numero2
			    return resultado

			# Ejemplo de uso
			numero1 = 5
			numero2 = 3
			print(sumar_numeros(numero1, numero2))  # Salida: 8

			```


		3. Desglose de los Conceptos en el Ejemplo:

		    Entrada:

		        'numero1' y 'numero2' son las entradas del algoritmo.


		    Salida:

		        El 'resultado', que es la suma de numero1 y numero2, es la salida.


		    Claridad y No Ambigüedad:

		        Cada paso está claramente definido: 

		        	leer los números, sumarlos y mostrar el resultado.


		    Efectividad:

		        Las operaciones de lectura, suma y muestra del resultado son básicas y realizables en un tiempo finito.


		    Finitud:

		        El algoritmo termina después de mostrar el resultado.


	Algoritmo de Ordenación por Inserción:

		Ordenar una lista de números usando 'Insertion Sort', un algoritmo sencilo y comúnmente utilizado para enseñar los conceptos básicos de ordenación y algoritmos en general.


		Descripción: 

			El algoritmo de ordenación por inserción construye la lista ordenada de manera gradual, un elemento a la vez, insertando cada nuevo elemento en su posición correcta en la parte ya ordenada de la lista.


		Pseudocódigo: 

			```
			Para i desde 1 hasta longitud de la lista - 1:
			    clave = lista[i]
			    j = i - 1
			    Mientras j >= 0 y lista[j] > clave:
			        lista[j + 1] = lista[j]
			        j = j - 1
			    lista[j + 1] = clave

			```


		Implementación: 

			```python

			def insertion_sort(lista):
			    for i in range(1, len(lista)):
			        clave = lista[i]
			        j = i - 1
			        while j >= 0 and lista[j] > clave:
			            lista[j + 1] = lista[j]
			            j = j - 1
			        lista[j + 1] = clave
			    return lista

			# Ejemplo de uso
			lista = [5, 2, 9, 1, 5, 6]
			lista_ordenada = insertion_sort(lista)
			print(lista_ordenada)  # Salida: [1, 2, 5, 5, 6, 9]

			```


		Paso a Paso:

			Inicialización:

			    Se comienza iterando desde el segundo elemento de la lista (i = 1) hasta el último elemento.


			Seleccionar la clave:

			    En cada iteración, se selecciona el elemento actual (clave = lista[i]) que se va a insertar en la parte ya ordenada de la lista.


			Comparación y Desplazamiento:

			    Se compara la clave con los elementos de la parte ordenada de la lista (los elementos antes de i).

			    Si clave es menor que lista[j], se desplaza lista[j] una posición hacia la derecha.

			    Este proceso se repite hasta que se encuentra la posición correcta para insertar clave.


			Inserción:

			    Una vez que se encuentra la posición correcta, clave se inserta en esa posición (lista[j + 1] = clave).


			Repetición:

			    El proceso se repite para todos los elementos de la lista hasta que toda la lista esté ordenada


		Análisis del Algoritmo:

		    Complejidad Temporal:

		        En el peor de los casos (cuando la lista está en orden inverso), la complejidad temporal es O(n^2), donde n es el número de elementos en la lista.

		        En el mejor de los casos (cuando la lista ya está ordenada), la complejidad temporal es O(n).


		    Complejidad Espacial:

		        La complejidad espacial es O(1) ya que el algoritmo utiliza una cantidad constante de espacio adicional.


		El algoritmo de ordenación por inserción es sencillo y efectivo para listas pequeñas o listas que ya están casi ordenadas.

		Aunque no es el más eficiente para listas grandes, su simplicidad y facilidad de implementación lo hacen ideal para enseñar los conceptos básicos de los algoritmos de ordenación.



|| Estructuras de Datos Básicas
		
	1. Arrays.

    2. Listas enlazadas.

    3. Pilas y colas.


    Estructuras de Datos: 

		Son una parte fundamental de la informática y la programación, y juegan un papel crucial en el diseño y análisis de algoritmos.

		Una estructura de datos es una forma específica de organizar y almacenar datos en una computadora de manera que puedan ser utilizados de manera eficiente.

		La elección de la estructura de datos adecuada puede influir significativamente en el rendimiento de un algoritmo.


	Definición:

	    Una estructura de datos es una colección de datos organizados y almacenados de manera que las operaciones sobre ellos puedan realizarse de manera eficiente.


	Tipos de Operaciones:

	    Inserción: 

	    	Añadir un nuevo elemento a la estructura.

	    Eliminación: 

	    	Quitar un elemento de la estructura.

	    Búsqueda:

	    	Encontrar un elemento dentro de la estructura.

	    Acceso: 

	    	Obtener un elemento en una posición específica.

	    Actualización: 

	    	Modificar un elemento en la estructura.


	Tipos de Estructuras de Datos: 

		1. Estructuras de Datos Lineales:

		    Los elementos se organizan en una secuencia lineal.


			Arrays (Arreglos):

			    Descripción:

			    	Colección de elementos de tamaño fijo, almacenados en ubicaciones de memoria contiguas.

			    Operaciones: 

			    	Acceso O(1), inserción/eliminación O(n) en el peor caso.
			    
			    Uso: 

			    	Útil cuando se necesita acceso rápido y directo a elementos por índice.


			Listas Enlazadas

			    Descripción: 

			    	Colección de nodos donde cada nodo contiene un valor y una referencia al siguiente nodo.

			    Tipos: 

			    	Lista enlazada simple, lista doblemente enlazada.

			    Operaciones: 

			    	Acceso O(n), inserción/eliminación O(1) cuando se tiene referencia al nodo.

			    Uso: 	

			    	Útil cuando se requiere inserción/eliminación frecuente y no se necesita acceso rápido por índice.


			Pilas (Stacks)

			    Descripción:

			    	Estructura LIFO (Last In, First Out), donde el último elemento añadido es el primero en ser eliminado.

			    Operaciones: 

			    	push (O(1)), pop (O(1)), peek (O(1)).

			    Uso: 

			    	Utilizadas en algoritmos de backtracking, evaluación de expresiones, etc.


			Colas (Queues)

			    Descripción:

			    	Estructura FIFO (First In, First Out), donde el primer elemento añadido es el primero en ser eliminado.

			    Tipos: 

			    	Cola simple, cola doblemente terminada (deque).

			    Operaciones: 

			    	enqueue (O(1)), dequeue (O(1)).

			    Uso: 

			    	Utilizadas en algoritmos de recorrido en amplitud, sistemas de gestión de tareas, etc.


		2. Estructuras de Datos No Lineales:

		    Los elementos se organizan en una estructura jerárquica o de red.


			Árboles:

			    Descripción: 

			   		Estructura jerárquica compuesta por nodos.

			    	Cada nodo tiene un valor y referencias a nodos hijos.

			    Tipos: 

			    	Árbol binario, árbol de búsqueda binaria (BST), árboles AVL, árboles B.

			    Operaciones:

			    	Búsqueda, inserción, eliminación varían entre O(log n) y O(n) dependiendo del tipo y balanceo.

			    Uso: 

			    	Utilizados en bases de datos, sistemas de archivos, algoritmos de búsqueda.


			Grafos

			    Descripción: 

			    	Conjunto de nodos (vértices) y aristas que conectan pares de nodos.

			    Tipos: 

			    	Grafos dirigidos, grafos no dirigidos, grafos ponderados.

			    Operaciones: 

			    	Búsqueda en profundidad (DFS), búsqueda en amplitud (BFS), caminos mínimos (Dijkstra).

			    Uso: 

			    	Modelar redes sociales, rutas de transporte, sistemas de recomendaciones.


			Tablas de Hash

			    Descripción:

			    	Estructura que mapea claves a valores usando una función hash para calcular el índice de la clave.

			    Operaciones: 

			    	Inserción, búsqueda, eliminación en O(1) en promedio.

			    Uso: 

			    	Implementaciones de diccionarios, caches, conjuntos.


	Usos y Comparación: 

		Ejemplo: 

			Búsqueda de un Elemento

	    Array: 

	    	Si se necesita buscar un elemento en un array desordenado, la complejidad es O(n). 

	    	Si el array está ordenado, se puede usar búsqueda binaria con complejidad O(log n).


	    Lista Enlazada: 

	    	La búsqueda en una lista enlazada desordenada también tiene complejidad O(n), pero no se puede usar búsqueda binaria incluso si la lista está ordenada, ya que no se puede acceder directamente a los elementos por índice.


	    Tabla de Hash: 

	    	La búsqueda tiene una complejidad promedio de O(1), lo que la hace muy eficiente para búsquedas rápidas.		


	Elección de la Estructura de Datos

		La elección de la estructura de datos adecuada depende de los requisitos específicos del problema a resolver.

		Factores como el tipo de operaciones que se realizarán con más frecuencia (búsqueda, inserción, eliminación), el tamaño de los datos y la necesidad de acceso directo o secuencial influyen en esta elección.


	1. Array: 

		Es una colección ordenada de elementos, todos del mismo tipo, almacenados en ubicaciones contiguas de memoria. 

		Cada elemento del array se puede acceder directamente mediante un índice, que generalmente comienza en 0.


		1. Características: 

		Tamaño Fijo:

	   		El tamaño de un array se define cuando se declara y no puede cambiar durante la ejecución del programa.


		Acceso Directo:

		    Los elementos de un array se pueden acceder directamente utilizando su índice. 

		    Esto proporciona un acceso muy rápido a los elementos, con una complejidad de tiempo O(1).


		Tipo Homogéneo:

		    Todos los elementos de un array deben ser del mismo tipo de datos (por ejemplo, todos enteros, todos caracteres, etc.).


		Memoria Contigua:

		    Los elementos de un array se almacenan en ubicaciones de memoria contiguas, lo que permite un acceso eficiente a los elementos	


		2. Operaciones:

		Acceso:

    		Acceder a un elemento en un array utilizando su índice.
    		
    		Complejidad: O(1).

    		```
    		elemento = array[indice]

    		```


    	Actualización:

    		Modificar el valor de un elemento en un array en una posición específica.
    		
    		Complejidad: O(1).

    		```
    		array[indice] = nuevo_valor

    		```


    	Búsqueda:

    		Buscar un elemento en un array (puede ser una búsqueda lineal o binaria si el array está ordenado).

			Complejidad: O(n) para búsqueda lineal, O(log n) para búsqueda binaria en un array ordenado


			```
			# Búsqueda lineal
			for i in range(len(array)):
			    if array[i] == valor_buscado:
			        return i

			```


		Inserción:

	    	Añadir un nuevo elemento en una posición específica (esto puede requerir el desplazamiento de otros elementos).
	    	
	    	Complejidad: O(n) en el peor caso (si se inserta al principio del array)

	    	```
	    	# Inserción en un array en Python
			array.insert(indice, nuevo_valor)

	    	```


    	Eliminación:

    		Eliminar un elemento de una posición específica (esto puede requerir el desplazamiento de otros elementos).
    		
    		Complejidad: O(n) en el peor caso (si se elimina el primer elemento).

    		```
    		# Eliminación en un array en Python
			array.pop(indice)

    		```


    	3. Uso de Arrays:

    	Ordenación: 	

    		Muchos algoritmos de ordenación, como Bubble Sort, Quick Sort y Merge Sort, utilizan arrays como estructura de datos base.

    		```python

    		# Ejemplo de Bubble Sort en Python
			def bubble_sort(array):
			    n = len(array)
			    for i in range(n):
			        for j in range(0, n-i-1):
			            if array[j] > array[j+1]:
			                array[j], array[j+1] = array[j+1], array[j]
			    return array

    		```


    	Recorrido:

    		Recorrer todos los elementos de un array para realizar operaciones como calcular la suma o el promedio de los elementos.

    		```python

    		# Calcular la suma de los elementos de un array
			def suma_array(array):
			    suma = 0
			    for elemento in array:
			        suma += elemento
			    return suma

			```


		Búsqueda:	

			Implementar algoritmos de búsqueda como la búsqueda lineal y la búsqueda binaria.

			```python

			# Búsqueda binaria en un array ordenado
			def busqueda_binaria(array, valor):
			    inicio = 0
			    fin = len(array) - 1
			    while inicio <= fin:
			        medio = (inicio + fin) // 2
			        if array[medio] == valor:
			            return medio
			        elif array[medio] < valor:
			            inicio = medio + 1
			        else:
			            fin = medio - 1
			    return -1

			```


		Ventajas y Desventajas:

		Ventajas: 

		Acceso Rápido:

		    Acceso O(1) a cualquier elemento mediante su índice.

		Simplicidad:

		    Fácil de implementar y usar.

		Eficiencia de Memoria:

		    Almacenamiento contiguo en memoria, lo que puede ser más eficiente en términos de uso de memoria


		Desventajas: 

		Tamaño Fijo:

		    No se puede cambiar el tamaño del array después de su declaración.

		Inserciones y Eliminaciones Costosas:

		    Las operaciones de inserción y eliminación pueden requerir el desplazamiento de muchos elementos, con una complejidad O(n).

		Homogeneidad:

		    Todos los elementos deben ser del mismo tipo, lo que puede ser una limitación en algunos contextos.


	2. Listas Enlazadas (Linked List):

		Se utiliza para organizar elementos de una manera dinámica y flexible.


		Definición:

			Una lista enlazada es una colección de nodos donde cada nodo contiene dos componentes: 

				un valor (o dato) y una referencia (o enlace) al siguiente nodo en la secuencia. 

			A diferencia de los arrays, las listas enlazadas no utilizan ubicaciones de memoria contiguas, lo que permite una mayor flexibilidad en la gestión de memoria.			

		Tipos de Listas Enlazadas:

			1. Lista Enlazada Simple (Singly Linked List):

    			Cada nodo tiene un enlace al siguiente nodo en la lista.

    			El último nodo tiene un enlace nulo (None o NULL).

    			```
    			[data|next] -> [data|next] -> ... -> [data|NULL]

    			```


    		2. Lista Doble Enlazada (Doubly Linked List):

    			Cada nodo tiene dos enlaces: 

    				uno al siguiente nodo y otro al nodo anterior.

   				Permite la navegación en ambas direcciones.

   				```
   				NULL <- [prev|data|next] <-> [prev|data|next] <-> ... <-> [prev|data|next] -> NULL

   				```


   			3. Lista Circular (Circular Linked List):

    			El último nodo de la lista enlaza de vuelta al primer nodo, formando un círculo.

    			Puede ser simple o doblemente enlazada

    			```
    			[data|next] -> [data|next] -> ... -> [data|next] -> [data|next]

    			```


    	Operaciones: 

    		Inserción:

   				Al inicio: 

   					Insertar un nuevo nodo al principio de la lista.

    			Al final: 

    				Insertar un nuevo nodo al final de la lista.

    			En medio: 

    				Insertar un nuevo nodo después de un nodo específico


    		```python

    		# Nodo de la lista enlazada
			class Nodo:
			    def __init__(self, dato):
			        self.dato = dato
			        self.siguiente = None

			# Lista enlazada simple
			class ListaEnlazada:
			    def __init__(self):
			        self.cabeza = None

			    # Inserción al inicio
			    def insertar_inicio(self, dato):
			        nuevo_nodo = Nodo(dato)
			        nuevo_nodo.siguiente = self.cabeza
			        self.cabeza = nuevo_nodo

    		```


    		Eliminación:

    			Del inicio: 

    				Eliminar el primer nodo de la lista.
    			
    			Del final: 

    				Eliminar el último nodo de la lista.

    			En medio: 

    				Eliminar un nodo específico


    		```python

    		# Eliminación de un nodo con un valor específico
			def eliminar(self, dato):
			    temp = self.cabeza
			    if temp is not None:
			        if temp.dato == dato:
			            self.cabeza = temp.siguiente
			            temp = None
			            return

			    while temp is not None:
			        if temp.dato == dato:
			            break
			        prev = temp
			        temp = temp.siguiente

			    if temp == None:
			        return

			    prev.siguiente = temp.siguiente
			    temp = None

    		```


    		Búsqueda:

   				Buscar un nodo que contiene un valor específico.

   			```python

   			# Búsqueda de un nodo con un valor específico
			def buscar(self, dato):
			    actual = self.cabeza
			    while actual is not None:
			        if actual.dato == dato:
			            return True
			        actual = actual.siguiente
			    return False

   			```


   			Recorrido:

    			Recorrer todos los nodos de la lista para realizar operaciones sobre ellos.

    		```python

    		# Recorrido de la lista
			def recorrer(self):
			    actual = self.cabeza
			    while actual is not None:
			        print(actual.dato, end=' ')
			        actual = actual.siguiente
			    print()

    		```


    	Ventajas y Desventajas:

    		Ventajas: 
    		
				Inserción/Eliminación Eficiente:

			    	Las operaciones de inserción y eliminación son más eficientes en comparación con los arrays cuando se realizan en el inicio o en el medio de la lista, con complejidad O(1).

				Tamaño Dinámico:

				    El tamaño de la lista puede crecer y disminuir dinámicamente, lo que permite una gestión de memoria más flexible.

				Sin Necesidad de Tamaño Predefinido:

				    No se requiere especificar el tamaño inicial de la lista.	


			Desventajas: 

				Acceso Secuencial:

				    El acceso a los elementos es secuencial, lo que significa que la búsqueda de un elemento específico tiene una complejidad O(n).
		
				Mayor Uso de Memoria:

				    Cada nodo adicional requiere espacio para almacenar un puntero, lo que puede aumentar el uso de memoria.

				Complejidad en la Implementación:

				    Las listas enlazadas son más complejas de implementar y gestionar en comparación con los arrays.	


		Usos: 	

			Implementación de Pilas y Colas:

    			Las pilas y colas pueden implementarse de manera eficiente utilizando listas enlazadas.


    		Algoritmos de Recorrido:

    			Recorrer estructuras complejas como árboles o grafos puede simplificarse utilizando listas enlazadas para gestionar las relaciones entre nodos.


    		Almacenamiento de Datos Dinámicos:

    			Utilizadas en situaciones donde el tamaño de los datos puede cambiar frecuentemente, como en aplicaciones de procesamiento de texto o sistemas de gestión de memoria.


	3. Pilas: 

		Se utilizan ampliamente en varios algoritmos debido a su naturaleza de Last In, First Out (LIFO).


		Definción: 

			Una pila es una estructura de datos lineal que sigue el principio de LIFO (Last In, First Out), lo que significa que el último elemento en entrar es el primero en salir. 

			Las pilas son útiles para tareas donde el orden de procesamiento es crucial, como en la evaluación de expresiones aritméticas, el manejo de llamadas a funciones y la gestión de backtracking


		Características: 	

			LIFO (Last In, First Out):

				El último elemento insertado en la pila es el primero en ser eliminado.


			Operaciones Básicas:

			    push: 

			    	Añadir un elemento al tope de la pila.

			    pop: 

			    	Eliminar y devolver el elemento del tope de la pila.

			    peek (o top):

			    	Devolver el elemento del tope de la pila sin eliminarlo.

			    isEmpty: 

			    	Comprobar si la pila está vacía


		Implementación de una Pila

			Las pilas se pueden implementar utilizando arrays o listas enlazadas. 

			A continuación, se muestra cómo se pueden implementar utilizando ambos enfoques.


			Array: 


			```python

			class PilaArray:
			    def __init__(self):
			        self.items = []

			    def is_empty(self):
			        return len(self.items) == 0

			    def push(self, item):
			        self.items.append(item)

			    def pop(self):
			        if self.is_empty():
			            return None
			        return self.items.pop()

			    def peek(self):
			        if self.is_empty():
			            return None
			        return self.items[-1]

			    def size(self):
			        return len(self.items)

			# Ejemplo de uso
			pila = PilaArray()
			pila.push(1)
			pila.push(2)
			print(pila.pop())  # Output: 2
			print(pila.peek())  # Output: 1
			print(pila.is_empty())  # Output: False


			```


			Linked List: 

			```python

			class Nodo:
			    def __init__(self, dato):
			        self.dato = dato
			        self.siguiente = None

			class PilaListaEnlazada:
			    def __init__(self):
			        self.cabeza = None

			    def is_empty(self):
			        return self.cabeza is None

			    def push(self, dato):
			        nuevo_nodo = Nodo(dato)
			        nuevo_nodo.siguiente = self.cabeza
			        self.cabeza = nuevo_nodo

			    def pop(self):
			        if self.is_empty():
			            return None
			        dato = self.cabeza.dato
			        self.cabeza = self.cabeza.siguiente
			        return dato

			    def peek(self):
			        if self.is_empty():
			            return None
			        return self.cabeza.dato

			    def size(self):
			        actual = self.cabeza
			        count = 0
			        while actual is not None:
			            count += 1
			            actual = actual.siguiente
			        return count

			# Ejemplo de uso
			pila = PilaListaEnlazada()
			pila.push(1)
			pila.push(2)
			print(pila.pop())  # Output: 2
			print(pila.peek())  # Output: 1
			print(pila.is_empty())  # Output: False

			```


		Operaciones:	

			push(item):

			    Añadir un elemento al tope de la pila.
			    Complejidad: O(1).

			pop():

			    Eliminar y devolver el elemento del tope de la pila.
			    Complejidad: O(1).

			peek():

			    Devolver el elemento del tope de la pila sin eliminarlo.
			    Complejidad: O(1).

			isEmpty():

			    Verificar si la pila está vacía.
			    Complejidad: O(1).


		Usos:

			Evaluación de Expresiones Aritméticas:

    			Las pilas se utilizan para evaluar expresiones en notación postfija (notación polaca inversa) y también para convertir infijas a postfijas.


    		Reversión de una Cadena:

    			Las pilas se pueden utilizar para invertir una cadena.

    			```python

    			def invertir_cadena(cadena):
				    pila = PilaArray()
				    for char in cadena:
				        pila.push(char)
				    cadena_invertida = ""
				    while not pila.is_empty():
				        cadena_invertida += pila.pop()
				    return cadena_invertida

				print(invertir_cadena("hola"))  # Output: "aloh"

    			```


    		Backtracking:

    			Las pilas son fundamentales en algoritmos de backtracking, como resolver laberintos, problemas de generación de combinaciones, y soluciones de problemas como las Torres de Hanoi.


    			```python

    			def torres_de_hanoi(n, origen, destino, auxiliar):
				    if n == 1:
				        print(f"Mover disco 1 de {origen} a {destino}")
				        return
				    torres_de_hanoi(n-1, origen, auxiliar, destino)
				    print(f"Mover disco {n} de {origen} a {destino}")
				    torres_de_hanoi(n-1, auxiliar, destino, origen)

				torres_de_hanoi(3, 'A', 'C', 'B')

    			```


    	Ventajas y Desventajas: 


    		Ventajas: 

    			Simplicidad:

			    	Fácil de implementar y utilizar.


				Eficiencia:

				    Operaciones push y pop eficientes con complejidad O(1)


    		Desventajas:

    			Acceso Limitado:

			    	Solo se puede acceder al elemento en el tope de la pila.


				No es Dinámico en Arrays:

			    	En una implementación basada en arrays, el tamaño de la pila puede estar limitado por el tamaño del array.



	4. Colas: 

		Se utilizan ampliamente en muchos algoritmos y aplicaciones.


		Definición:

			Es una estructura de datos lineal que sigue el principio de First In, First Out (FIFO), lo que significa que el primer elemento en entrar es el primero en salir. 

			Las colas son útiles para gestionar tareas en las que el orden de llegada es importante, como en la gestión de procesos en sistemas operativos, en sistemas de impresión y en el manejo de eventos.


		Características:

			FIFO (First In, First Out):

    			El primer elemento en ser añadido a la cola es el primero en ser eliminado.


    		Operaciones Básicas:

    			enqueue: 

    				Añadir un elemento al final de la cola.
    			
    			dequeue: 

    				Eliminar y devolver el elemento del frente de la cola.

				front:

					Devolver el elemento del frente de la cola sin eliminarlo.

				isEmpty: 

					Comprobar si la cola está vacía


		Implementación: 

			Se pueden implementar utilizando arrays (o listas en Python) o listas enlazadas.	

			Array: 

			```python

			class ColaArray:
			    def __init__(self):
			        self.items = []

			    def is_empty(self):
			        return len(self.items) == 0

			    def enqueue(self, item):
			        self.items.append(item)

			    def dequeue(self):
			        if self.is_empty():
			            return None
			        return self.items.pop(0)

			    def front(self):
			        if self.is_empty():
			            return None
			        return self.items[0]

			    def size(self):
			        return len(self.items)

			# Ejemplo de uso
			cola = ColaArray()
			cola.enqueue(1)
			cola.enqueue(2)
			print(cola.dequeue())  # Output: 1
			print(cola.front())    # Output: 2
			print(cola.is_empty()) # Output: False

			```


			Linked List: 

			```python

			class Nodo:
			    def __init__(self, dato):
			        self.dato = dato
			        self.siguiente = None

			class ColaListaEnlazada:
			    def __init__(self):
			        self.frente = None
			        self.final = None

			    def is_empty(self):
			        return self.frente is None

			    def enqueue(self, dato):
			        nuevo_nodo = Nodo(dato)
			        if self.final:
			            self.final.siguiente = nuevo_nodo
			        self.final = nuevo_nodo
			        if self.frente is None:
			            self.frente = nuevo_nodo

			    def dequeue(self):
			        if self.is_empty():
			            return None
			        dato = self.frente.dato
			        self.frente = self.frente.siguiente
			        if self.frente is None:
			            self.final = None
			        return dato

			    def front(self):
			        if self.is_empty():
			            return None
			        return self.frente.dato

			    def size(self):
			        actual = self.frente
			        count = 0
			        while actual:
			            count += 1
			            actual = actual.siguiente
			        return count

			# Ejemplo de uso
			cola = ColaListaEnlazada()
			cola.enqueue(1)
			cola.enqueue(2)
			print(cola.dequeue())  # Output: 1
			print(cola.front())    # Output: 2
			print(cola.is_empty()) # Output: False

			```


		Operaciones:

			enqueue(item):

    			Añadir un elemento al final de la cola.
    			
    			Complejidad: O(1).

			dequeue():

			    Eliminar y devolver el elemento del frente de la cola.
			    
			    Complejidad: O(1).
						
			front():

    			Devolver el elemento del frente de la cola sin eliminarlo.
    			
    			Complejidad: O(1).

			isEmpty():

    			Verificar si la cola está vacía.
    			
    			Complejidad: O(1).    		


    	Tipos de Cola: 

    		Cola Simple:

    			Implementación básica con operaciones FIFO.

    		Cola Doble (Deque o Double-ended Queue):

    			Permite la inserción y eliminación de elementos en ambos extremos de la cola.

			Cola Prioritaria:

   	 			Cada elemento tiene una prioridad y los elementos con mayor prioridad se eliminan antes, independientemente de su orden de llegada.   		


   	 	Usos: 

   	 		Gestión de Tareas en Sistemas Operativos:

    			Las colas se utilizan para gestionar procesos y tareas en sistemas operativos, donde los procesos llegan en un orden y se ejecutan en ese mismo orden.

    		Sistemas de Impresión:

    			Los trabajos de impresión se gestionan en una cola donde el primer documento en llegar es el primero en ser impreso.

    		Búsqueda en Anchura (Breadth-First Search, BFS):

    			En algoritmos de grafos, BFS utiliza una cola para explorar vértices en niveles.


    		Simulación de Colas:

    			En simulaciones de sistemas como colas de banco o colas de atención al cliente, las colas se utilizan para gestionar el orden de servicio.


    	Ventajas y Desventajas:

    		Ventajas: 

    			Simplicidad:

			    	Fácil de implementar y utilizar.

				Eficiencia:

			    	Operaciones enqueue y dequeue eficientes con complejidad O(1).


    		Desventajas:

    			Acceso Limitado:

			    	Solo se puede acceder al elemento en el frente de la cola para eliminación y al final para inserción.

				No es Dinámico en Arrays:

				    En una implementación basada en arrays, el tamaño de la cola puede estar limitado por el tamaño del array.



|| Búsqueda Lineal y Búsqueda Binaria
	

	Búsqueda Lineal: 

		Algoritmo sencillo y fundamental utilizado para encontrar un elemento en una lista o arreglo. 

		Se caracteriza por su simplicidad y es adecuado para listas pequeñas o cuando no hay ninguna información adicional sobre el orden de los elementos en la lista.


		Definición:

			La búsqueda lineal es un método de búsqueda que examina cada elemento de una lista, uno por uno, hasta encontrar el elemento deseado o hasta que todos los elementos hayan sido revisados.

	
		Complejidad Temporal: 	

    		En el peor de los casos, la búsqueda lineal tiene una complejidad temporal de O(n), donde nn es el número de elementos en la lista.

    		En el mejor de los casos, si el elemento buscado es el primero en la lista, la complejidad es O(1).


    	Uso: 

    		Es útil cuando la lista es pequeña o cuando no se conoce el orden de los elementos en la lista.


    	Implementación: 

    		```
    		function linear_search(arr, target):
			    for i from 0 to length(arr) - 1:
			        if arr[i] == target:
			            return i
			    return -1  # Elemento no encontrado

    		```

    		```python

    		def linear_search(arr, target):
			    for i in range(len(arr)):
			        if arr[i] == target:
			            return i
			    return -1  # Elemento no encontrado

			# Ejemplo de uso
			arr = [4, 2, 3, 1, 5]
			target = 3
			result = linear_search(arr, target)
			print(f"Elemento encontrado en el índice: {result}")  # Salida: Elemento encontrado en el índice: 2


    		```


    	Ventajas y Desventajas: 

    		Ventajas: 

    			Simplicidad: 

    				El algoritmo es fácil de entender e implementar.

				Sin Requisitos Previos: 

					No se requiere que la lista esté ordenada.

				Espacio Constante:

					Utiliza una cantidad constante de memoria adicional O(1)


			Desventajas: 

				Ineficiencia: 

					Puede ser lento para listas grandes debido a su complejidad O(n).

				No Aprovecha Orden:

					No aprovecha si la lista está ordenada, a diferencia de algoritmos como la búsqueda binaria

		Aplicaciones: 

			Problemas de Tamaño Pequeño:

		    	Adecuada para listas pequeñas donde la eficiencia no es un problema crítico.

			Verificación de Existencia:

			    Útil cuando se necesita verificar rápidamente la existencia de un elemento en una lista.

			Búsqueda en Listas No Ordenadas:

			    Ideal cuando no se tiene información sobre el orden de los elementos.


		Ejemplo: 

			Eenemos una lista de nombres y queremos verificar si un nombre específico está en la lista.

			```python

			def linear_search_names(names, target_name):
			    for index, name in enumerate(names):
			        if name == target_name:
			            return index
			    return -1

			names = ["Alice", "Bob", "Charlie", "David"]
			target_name = "Charlie"
			result = linear_search_names(names, target_name)
			print(f"Nombre encontrado en el índice: {result}")  # Salida: Nombre encontrado en el índice: 2


			```


	Búsqueda Binaria:

		Es un algoritmo de búsqueda eficiente que se utiliza para encontrar un elemento en una lista ordenada.

		Aprovecha el hecho de que la lista está ordenada para reducir significativamente el número de comparaciones necesarias para encontrar el elemento deseado.


		Definición:

			La búsqueda binaria es un método de búsqueda que divide repetidamente a la mitad el rango de posibles ubicaciones del elemento buscado hasta que el rango se reduce a uno solo.


		Precondición:

    		La lista debe estar ordenada de manera ascendente (o descendente).

		
		Complejidad Temporal:

    		La complejidad temporal de la búsqueda binaria es O(log⁡ n), donde n es el número de elementos en la lista.		


    	Implementación: 

    		```
    		function binary_search(arr, target):
			    low = 0
			    high = length(arr) - 1

			    while low <= high:
			        mid = low + (high - low) / 2  # Evitar overflow

			        if arr[mid] == target:
			            return mid
			        elif arr[mid] < target:
			            low = mid + 1
			        else:
			            high = mid - 1

			    return -1  # Elemento no encontrado

    		```


    		```python

			def binary_search(arr, target):
			    low = 0
			    high = len(arr) - 1

			    while low <= high:
			        mid = (low + high) // 2  # Encuentra el punto medio

			        if arr[mid] == target:
			            return mid
			        elif arr[mid] < target:
			            low = mid + 1
			        else:
			            high = mid - 1

			    return -1  # Elemento no encontrado

			# Ejemplo de uso
			arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
			target = 7
			result = binary_search(arr, target)
			print(f"Elemento encontrado en el índice: {result}")  # Salida: Elemento encontrado en el índice: 6

    		```


    	Análisis del Algoritmo

		    Mejor Caso:

		        El elemento buscado se encuentra en la posición media en el primer intento.

		        Complejidad: O(1)O(1).

		    Peor Caso:

		        El elemento buscado no está en la lista, o se encuentra al final de la lista.

		        Complejidad: O(log⁡ n).

		    Caso Promedio:

		        En promedio, la búsqueda binaria requiere O(log⁡ n) comparaciones.


		Ventajas y Desventajas:

			Ventajas: 

				Eficiencia: 

					Mucho más rápido que la búsqueda lineal para listas grandes debido a su complejidad O(log⁡ n).

				Menor Número de Comparaciones:

					Reduce significativamente el número de comparaciones necesarias.


			Desventajas: 

				Requiere Lista Ordenada: 

					La lista debe estar ordenada antes de realizar la búsqueda.


				Complejidad de Implementación:

					Aunque no es extremadamente complejo, es más difícil de implementar correctamente en comparación con la búsqueda lineal.


		Variante recursiva: 

			La búsqueda binaria puede implementarse de manera recursiva

			```python

			def binary_search_recursive(arr, target, low, high):
			    if low > high:
			        return -1  # Elemento no encontrado

			    mid = (low + high) // 2

			    if arr[mid] == target:
			        return mid
			    elif arr[mid] < target:
			        return binary_search_recursive(arr, target, mid + 1, high)
			    else:
			        return binary_search_recursive(arr, target, low, mid - 1)

			# Ejemplo de uso
			arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
			target = 7
			result = binary_search_recursive(arr, target, 0, len(arr) - 1)
			print(f"Elemento encontrado en el índice: {result}")  # Salida: Elemento encontrado en el índice: 6

			```


		Aplicaciones: 

			Problemas de Búsqueda:

		    	Encontrar un valor específico en listas ordenadas, como bases de datos o directorios.

			Problemas de Decisión:

		    	Determinar si un valor pertenece a un conjunto ordenado de datos.

			Encontrar el Punto de Ruptura:

		    	Identificar el punto en el que una función o secuencia cambia su comportamiento.			



|| Ordenación

	Se refiere a la clasificación de elementos en una secuencia o estructura de datos según un criterio específico, como valores numéricos, caracteres alfabéticos, etc. 

	La ordenación es una operación fundamental y común en la informática, ya que muchos otros algoritmos dependen de listas ordenadas para funcionar eficientemente.


	Definición:

	    Ordenar una lista o arreglo significa reorganizar sus elementos en un orden específico, típicamente ascendente o descendente.


	Importancia:

	    La ordenación facilita otras operaciones, como búsqueda binaria, fusiones eficientes, y optimización de algoritmos.

	    Muchos problemas se simplifican considerablemente si los datos están ordenados.


	Tipos de Algoritmos de Ordenación

		1. Ordenación por Intercambio

		    Bubble Sort (Ordenación de Burbuja):

		        Compara y cambia adyacentes repetidamente si están en el orden incorrecto.

		        Complejidad Temporal: 

		        	O(n^2).
		        
		        Uso: 

		        	Didáctico y para listas muy pequeñas.

		    ```python

		    def bubble_sort(arr):
			    n = len(arr)
			    for i in range(n):
			        for j in range(0, n-i-1):
			            if arr[j] > arr[j+1]:
			                arr[j], arr[j+1] = arr[j+1], arr[j]
			    return arr


		    ```


		2. Ordenación por Selección

		    Selection Sort (Ordenación por Selección):

		        Encuentra repetidamente el elemento mínimo (o máximo) de la lista y lo coloca en su posición correcta.

		        Complejidad Temporal: 

		        	O(n^2).

		        Uso: 

		        	Didáctico y para listas pequeñas

		    ```python

		    def selection_sort(arr):
			    n = len(arr)
			    for i in range(n):
			        min_idx = i
			        for j in range(i+1, n):
			            if arr[j] < arr[min_idx]:
			                min_idx = j
			        arr[i], arr[min_idx] = arr[min_idx], arr[i]
			    return arr

		    ```


		3. Ordenación por Inserción

		    Insertion Sort (Ordenación por Inserción):

		        Construye la lista ordenada un elemento a la vez, tomando un elemento de la lista de entrada y ubicándolo en la posición correcta.

		        Complejidad Temporal: 

		        	O(n^2).

		        Uso: 

		        	Eficiente para listas pequeñas y parcialmente ordenadas.

		    ```python

		    def insertion_sort(arr):
			    n = len(arr)
			    for i in range(1, n):
			        key = arr[i]
			        j = i-1
			        while j >= 0 and key < arr[j]:
			            arr[j+1] = arr[j]
			            j -= 1
			        arr[j+1] = key
			    return arr

		    ```


		4. Ordenación por Mezcla

		    Merge Sort (Ordenación por Mezcla):

		        Divide la lista en mitades, ordena cada mitad y luego las fusiona.

		        Complejidad Temporal: 

		        	O(n log ⁡n).

		        Uso: 

		        	Eficiente y estable, adecuado para listas grandes

		    ```python

		    def merge_sort(arr):
			    if len(arr) > 1:
			        mid = len(arr) // 2
			        L = arr[:mid]
			        R = arr[mid:]

			        merge_sort(L)
			        merge_sort(R)

			        i = j = k = 0
			        while i < len(L) and j < len(R):
			            if L[i] < R[j]:
			                arr[k] = L[i]
			                i += 1
			            else:
			                arr[k] = R[j]
			                j += 1
			            k += 1

			        while i < len(L):
			            arr[k] = L[i]
			            i += 1
			            k += 1

			        while j < len(R):
			            arr[k] = R[j]
			            j += 1
			            k += 1

			    return arr

		    ```


		5. Ordenación por División: 

			Quick Sort (Ordenación Rápida):

			    Selecciona un "pivote" y particiona la lista de modo que los elementos menores que el pivote están a su izquierda y los mayores a su derecha, y luego ordena recursivamente las sublistas.

			    Complejidad Temporal: 

			    	Promedio O(n log⁡ n), Peor caso O(n^2) (mitigado con técnicas como elección aleatoria del pivote).

			    Uso: 

			    	Muy eficiente en la práctica y ampliamente utilizado.

			```python

			def quick_sort(arr):
			    if len(arr) <= 1:
			        return arr
			    else:
			        pivot = arr[len(arr) // 2]
			        left = [x for x in arr if x < pivot]
			        middle = [x for x in arr if x == pivot]
			        right = [x for x in arr if x > pivot]
			        return quick_sort(left) + middle + quick_sort(right)

			```


	Consideraciones:

	    Estabilidad:

	        Un algoritmo de ordenación es estable si mantiene el orden relativo de los elementos iguales.

	        Ejemplo: 

	        	Merge Sort es estable, mientras que Quick Sort no lo es en su implementación básica.

	    Complejidad Espacial:

	        Algunos algoritmos requieren espacio adicional significativo (por ejemplo, Merge Sort), mientras que otros pueden funcionar en lugar (por ejemplo, Quick Sort).

	    Adaptabilidad:

	        Algunos algoritmos funcionan mejor con listas parcialmente ordenadas (por ejemplo, Insertion Sort).


	Uso:  

		Tenemos una lista de números y queremos compararla usando diferentes algoritmos de ordenación.


		```python

		arr = [64, 34, 25, 12, 22, 11, 90]

		# Ordenación de Burbuja
		print("Bubble Sort:", bubble_sort(arr.copy()))

		# Ordenación por Selección
		print("Selection Sort:", selection_sort(arr.copy()))

		# Ordenación por Inserción
		print("Insertion Sort:", insertion_sort(arr.copy()))

		# Ordenación por Mezcla
		print("Merge Sort:", merge_sort(arr.copy()))

		# Ordenación Rápida
		print("Quick Sort:", quick_sort(arr.copy()))


		```



|| Complejidad Algorítmica

	1. Notación Asintótica:

   		Big-O, Big-Theta, Big-Omega.


	2. Análisis de Complejidad

    	Ejemplos prácticos.
    	
    	Comparación de algoritmos.


    Complejidad Temporal: 

		Es una medida de cuánto tiempo tarda en ejecutarse en función del tamaño de su entrada. 

		Esta medida es crucial para evaluar la eficiencia de un algoritmo, especialmente cuando se trabaja con grandes conjuntos de datos.


	Definición:

	    La complejidad temporal estima el tiempo de ejecución de un algoritmo en función del tamaño de la entrada. 

	    Se expresa típicamente usando la notación Big-O, que describe el comportamiento asintótico del tiempo de ejecución cuando el tamaño de la entrada tiende a infinito.


	Notación Big-O:

	    La notación Big-O describe un límite superior en el tiempo de ejecución. 

	    Por ejemplo, si decimos que un algoritmo tiene una complejidad O(n), significa que el tiempo de ejecución del algoritmo crece linealmente con el tamaño de la entrada.


	Tipos de Complejidad Temporal:

		O(1) - Constante:

		    El tiempo de ejecución es constante y no depende del tamaño de la entrada.

		    Ejemplo: 

		    	Acceder a un elemento en un array por índice.


		O(log n) - Logarítmica:

		    El tiempo de ejecución crece logarítmicamente con el tamaño de la entrada. 

		    Ejemplo: 

		    	búsqueda binaria.


		O(n) - Lineal:

		    El tiempo de ejecución crece linealmente con el tamaño de la entrada. 

		    Ejemplo: 

		    	recorrer todos los elementos de un array.


		O(n log n) - Linealítmica:

		    El tiempo de ejecución es una combinación de lineal y logarítmica. 

		    Ejemplo: 

		    	algoritmos de ordenación eficientes como Merge Sort y Quick Sort.


		O(n^2) - Cuadrática:

		    El tiempo de ejecución crece con el cuadrado del tamaño de la entrada.

		    Ejemplo: 

		    	algoritmos de ordenación menos eficientes como Bubble Sort y Insertion Sort.


		O(2^n) - Exponencial:

		    El tiempo de ejecución crece exponencialmente con el tamaño de la entrada. 

		    Ejemplo: 

		    	algunos algoritmos de fuerza bruta para resolver problemas de combinatoria.


	Análisis de Complejidad Temporal del Algoritmo Insertion Sort: 

		Algoritmo de ordenación menos eficientes, con un tiempo de ejecución de entrada O(n^2) - Cuadrática:

		```python

		def insertion_sort(lista):
		    for i in range(1, len(lista)):
		        clave = lista[i]
		        j = i - 1
		        while j >= 0 and lista[j] > clave:
		            lista[j + 1] = lista[j]
		            j = j - 1
		        lista[j + 1] = clave
		    return lista

		```

		Inicialización del Bucle Externo:

	        El bucle externo (for i in range(1, len(lista))) se ejecuta n-1 veces, donde n es el número de elementos en la lista.


	    Bucle Interno:

	        En el peor de los casos, el bucle interno (while j >= 0 and lista[j] > clave) también se ejecuta n-1 veces para cada iteración del bucle externo.


	    Número Total de Comparaciones y Desplazamientos:

	        En el peor de los casos (cuando la lista está ordenada en orden inverso), el número total de comparaciones y desplazamientos es proporcional a la suma de los primeros n-1 números enteros: 

	        	1+2+3+...+(n−1)=(n−1)n/2.


	    Complejidad Temporal:

	        Por lo tanto, la complejidad temporal en el peor de los casos es O(n^2).


	    Importancia de la Complejidad Temporal

		    Eficiencia: 

		    	La complejidad temporal nos ayuda a entender cómo se comportará el algoritmo a medida que crece el tamaño de la entrada, lo cual es crucial para aplicaciones de la vida real donde los datos pueden ser muy grandes.


		    Comparación: 

		    	Permite comparar diferentes algoritmos y seleccionar el más adecuado para un problema dado basado en su eficiencia.


		    Optimización: 

		    	Conocer la complejidad temporal ayuda a identificar cuellos de botella y áreas donde el algoritmo puede ser mejorado.



|| Complejidad Espacial

	Se refiere a la cantidad de memoria que necesita para su ejecución en función del tamaño de la entrada. 

	Es un aspecto crucial en el análisis de algoritmos, ya que afecta directamente la eficiencia y viabilidad de su implementación, especialmente en sistemas con recursos limitados.


	Definición:

    	La complejidad espacial mide el espacio total requerido por un algoritmo, que incluye tanto el espacio para los datos de entrada como el espacio adicional que el algoritmo necesita para su procesamiento.
	

    Componentes de la Complejidad Espacial:

    	Espacio de Entrada:

    		Memoria requerida para almacenar los datos de entrada.

    	Espacio Auxiliar: 

    		Memoria adicional utilizada por el algoritmo durante su ejecución, como variables temporales, estructuras de datos auxiliares, etc.

    	Notación Asintótica:

    		Al igual que la complejidad temporal, la complejidad espacial se expresa usando notaciones como O, Ω y Θ para describir el crecimiento del espacio en función del tamaño de la entrada (n).


    Análisis de complejidad espacial en Algoritmos: 

    	Búsqueda Lineal

			La búsqueda lineal revisa cada elemento de una lista para encontrar un valor objetivo.

			```python

			def linear_search(arr, target):
			    for i in range(len(arr)):
			        if arr[i] == target:
			            return i
			    return -1

			```

			Complejidad Espacial: O(1).

        		El algoritmo utiliza una cantidad constante de espacio adicional, independientemente del tamaño de la lista.


        Búsqueda Binaria

			La búsqueda binaria funciona en listas ordenadas y divide el rango de búsqueda a la mitad en cada paso.

			```python

			def binary_search(arr, target):
			    low = 0
			    high = len(arr) - 1

			    while low <= high:
			        mid = (low + high) // 2

			        if arr[mid] == target:
			            return mid
			        elif arr[mid] < target:
			            low = mid + 1
			        else:
			            high = mid - 1

			    return -1

			```


		Merge Sort (Ordenación por Mezcla):

			Merge Sort es un algoritmo de ordenación que utiliza el enfoque de dividir y conquistar.

			```python

			def merge_sort(arr):
			    if len(arr) > 1:
			        mid = len(arr) // 2
			        L = arr[:mid]
			        R = arr[mid:]

			        merge_sort(L)
			        merge_sort(R)

			        i = j = k = 0
			        while i < len(L) and j < len(R):
			            if L[i] < R[j]:
			                arr[k] = L[i]
			                i += 1
			            else:
			                arr[k] = R[j]
			                j += 1
			            k += 1

			        while i < len(L):
			            arr[k] = L[i]
			            i += 1
			            k += 1

			        while j < len(R):
			            arr[k] = R[j]
			            j += 1
			            k += 1

			    return arr

			```

			Complejidad Espacial: O(n):

    			Utiliza espacio adicional para almacenar las sublistas LL y RR, resultando en un espacio auxiliar lineal.


    	Quick Sort (Ordenación Rápida):

			Quick Sort es otro algoritmo de ordenación eficiente que también usa el enfoque de dividir y conquistar.

			```python

			def quick_sort(arr):
			    if len(arr) <= 1:
			        return arr
			    else:
			        pivot = arr[len(arr) // 2]
			        left = [x for x in arr if x < pivot]
			        middle = [x for x in arr if x == pivot]
			        right = [x for x in arr if x > pivot]
			        return quick_sort(left) + middle + quick_sort(right)

			```

			Complejidad Espacial:

    			En el peor de los casos:

    				O(n), debido a las llamadas recursivas que pueden usar hasta n niveles de pila.
    		

    			En el mejor y promedio de los casos: 

    				O(log⁡ n) si se implementa en lugar (in-place) y de manera óptima.


    Consideraciones:

    	Eficiencia de Memoria:

		    En sistemas con memoria limitada, es crucial seleccionar algoritmos que utilicen la menor cantidad de espacio adicional posible.

		Impacto en el Rendimiento:

		    Un uso excesivo de memoria puede provocar intercambios frecuentes con la memoria secundaria (paginación), lo que afecta negativamente el rendimiento del algoritmo.

		Escalabilidad:

		    La complejidad espacial afecta la capacidad de un algoritmo para manejar grandes conjuntos de datos.

		    Algoritmos con baja complejidad espacial son más escalables.


	Implementación: 

		Para ilustrar cómo la complejidad espacial afecta la selección del algoritmo, consideremos dos métodos para revertir una lista.


		Método 1: Uso de lista auxiliar

			```python

			def reverse_list_aux(arr):
			    n = len(arr)
			    reversed_arr = [0] * n
			    for i in range(n):
			        reversed_arr[i] = arr[n - i - 1]
			    return reversed_arr


			``` 

			Complejidad Espacial: O(n):

    			Utiliza espacio adicional proporcional al tamaño de la lista original.


    	Método 2: In-place.

    		```python

    		def reverse_list_in_place(arr):
			    left = 0
			    right = len(arr) - 1
			    while left < right:
			        arr[left], arr[right] = arr[right], arr[left]
			        left += 1
			        right -= 1
			    return arr

    		```

    		Complejidad Espacial: O(1)

    			Requiere una cantidad constante de espacio adicional, ya que la reversión se realiza dentro de la misma lista.



|| Big-O
	
	Es una forma de describir la eficiencia de un algoritmo en términos de su rendimiento y uso de recursos, específicamente tiempo y espacio. 

	Esta notación se centra en el comportamiento asintótico del algoritmo, es decir, cómo se comporta cuando el tamaño de la entrada se aproxima al infinito.


	Definición:

		Big-O describe una cota superior asintótica para la complejidad de un algoritmo.

		En otras palabras, proporciona una estimación del máximo número de operaciones que un algoritmo realizará en función del tamaño de la entrada.


	Propósito:

		Ayuda a comparar la eficiencia de diferentes algoritmos y elegir el más adecuado para un problema específico.


	Formulación:

		Formalmente, decimos que una función f(n) es O(g(n)) si existen constantes positivas c y n_0​ tales que f(n)≤c⋅g(n) para todo n≥n_0.



	Ejemplos: 

		1. O(1) - Constante:

    		La complejidad es constante si el tiempo de ejecución no cambia con el tamaño de la entrada.

    		Acceder a un elemento de un array por su índice:

    		```python

    		def get_first_element(arr):
    			return arr[0]

    		```


    	2. O(n) - Lineal:

    		La complejidad es lineal si el tiempo de ejecución crece de manera proporcional al tamaño de la entrada.

    		Recorrer una lista y sumar sus elementos:

    		```python

    		def sum_elements(arr):
			    total = 0
			    for element in arr:
			        total += element
			    return total

    		```


		3. O(n^2) - Cuadrática:

    		La complejidad es cuadrática si el tiempo de ejecución es proporcional al cuadrado del tamaño de la entrada.

    		Ordenar una lista usando Bubble Sort.

    		```python

    		def bubble_sort(arr):
			    n = len(arr)
			    for i in range(n):
			        for j in range(0, n-i-1):
			            if arr[j] > arr[j+1]:
			                arr[j], arr[j+1] = arr[j+1], arr[j]

    		```  

		
		4. O(logn) - Logarítmica:

    		La complejidad es logarítmica si el tiempo de ejecución crece de manera logarítmica con el tamaño de la entrada.

    		Búsqueda binaria en una lista ordenada:

    		```python

    		def binary_search(arr, target):
			    low = 0
			    high = len(arr) - 1

			    while low <= high:
			        mid = (low + high) // 2

			        if arr[mid] == target:
			            return mid
			        elif arr[mid] < target:
			            low = mid + 1
			        else:
			            high = mid - 1

			    return -1

    		```		


    	5. O(nlogn) - Lineal Logarítmica:

    		La complejidad es lineal logarítmica si el tiempo de ejecución es proporcional al tamaño de la entrada multiplicado por el logaritmo del tamaño de la entrada.

    		Ordenar una lista usando Merge Sort.

    		```python

    		def merge_sort(arr):
			    if len(arr) > 1:
			        mid = len(arr) // 2
			        L = arr[:mid]
			        R = arr[mid:]

			        merge_sort(L)
			        merge_sort(R)

			        i = j = k = 0
			        while i < len(L) and j < len(R):
			            if L[i] < R[j]:
			                arr[k] = L[i]
			                i += 1
			            else:
			                arr[k] = R[j]
			                j += 1
			            k += 1

			        while i < len(L):
			            arr[k] = L[i]
			            i += 1
			            k += 1

			        while j < len(R):
			            arr[k] = R[j]
			            j += 1
			            k += 1

			    return arr

    		```


    Reglas y Propiedades de Big-O:

    	1. Constantes y Coeficientes:

    		En la notación Big-O, las constantes y los coeficientes se omiten porque el enfoque está en el crecimiento asintótico.

    		Ejemplo: O(2n) y O(3n) se simplifican a O(n).


    	2. Términos Dominantes:

    		Solo se considera el término dominante en la notación Big-O.

    		Ejemplo: O(n^2+n) se simplifica a O(n^2).


    	3. Sumas de Complejidades:

		    Si un algoritmo realiza dos operaciones secuenciales con complejidades O(f(n)) y O(g(n)), la complejidad combinada es O(f(n)+g(n)), y se toma el término dominante.

		    Ejemplo: Si una función tiene partes O(n) y O(n^2), la complejidad total es O(n^2).


		4. Multiplicación de Complejidades:

    		Si un algoritmo tiene una estructura anidada (por ejemplo, un bucle dentro de otro), se multiplican las complejidades.

    		Ejemplo: Un bucle O(n) dentro de otro bucle O(n)O(n) resulta en O(n×n)=O(n^2)


    Ejemplo comparativo: 

    	Función que realiza una búsqueda lineal seguida de una ordenación por burbuja

    	```python

    	def example_function(arr, target):
		    # Búsqueda lineal: O(n)
		    for i in range(len(arr)):
		        if arr[i] == target:
		            return True

		    # Ordenación por burbuja: O(n^2)
		    n = len(arr)
		    for i in range(n):
		        for j in range(0, n-i-1):
		            if arr[j] > arr[j+1]:
		                arr[j], arr[j+1] = arr[j+1], arr[j]
		    
		    return False

    	```

	    Búsqueda Lineal: O(n)
		
		Ordenación por Burbuja: O(n^2).
		
		Complejidad Total: O(n)+O(n^2) = O(n^2) (se toma el término dominante).



|| Análisis de Algoritmos

	Es una rama de las ciencias de la computación que estudia el rendimiento de los algoritmos, especialmente su tiempo de ejecución y requerimientos de espacio.

	El objetivo práctico del análisis de algoritmos es predecir el rendimiento de diferentes algoritmos con el fin de guiar decisiones de diseño.

	Por ejemplo, responder "la manera más eficiente para ordenar un millón de enteros de 32 bit."

	Usando el ordenamiento de burbuja (bubble sort) o el ordenamiento radix. 

	El ordenamiento de burbuja es simple pero lento para bases de datos grandes. 

	El ordenamiento radix que es muy rapido y eficiente cuando se trata de ordenar linealmente grandes grupos de números cortos pero no funciona tan bien con números extensos.  


	El objetivo del análisis de algoritmos es hacer comparaciones significativas entre algoritmos, pero hay algunos problemas:

		1. El rendimiento relativo de los algoritmos podría depender de características del hardware, por lo cual un algoritmo podría ser más rápido en la 'Máquina A' y otro en la 'Máquina B'. 

		La solución general a este problema es especificar un modelo de máquina y analizar el número de pasos, u operaciones, que un algoritmo requiere según un modelo de máquina dado.


		[Respecto a Radix Sort, si tienes una pregunta como esta en una entrevista, pienso que una mejor respuesta es, “La manera más rápida de ordenar un millón de enteros es utilizar cualquier función de ordenamiento que sea proporcionada por el lenguaje que estoy utilizando. 

		Su rendimiento es suficientemente bueno para la gran mayoría de las aplicaciones, pero si resulta que mi aplicación fue muy lenta, utilizaría un analizador de rendimiento para ver dónde fue utilizado el tiempo. 

		Si pareciera que un algoritmo de ordenamiento más rápido tendría un efecto importante en el rendimiento, entonces buscaría una buena implementación del ordenamiento radix.”]


		2. El rendimiento relativo podría depender de los detalles del conjunto de datos. 

		Por ejemplo, algunos algoritmos de ordenamiento se ejecutan de manera más rápida si los datos ya están parcialmente ordenados; otros algoritmos se ejecutan de manera más lenta en este caso. 

		Una manera común de evitar este problema es analizar el peor de los casos. 

		A veces es útil analizar el rendimiento del caso promedio, pero eso es generalmente más difícil, y el conjunto de casos sobre el cual se establece el promedio podría no ser obvio.


		3. El rendimiento relativo depende también del tamaño del problema. 

		Un algoritmo de ordenamiento que es rápido para listas pequeñas podría ser lento para listas largas.

		La solución usual a este problema es expresar el tiempo de ejecución (o número de operaciones) como una función del tamaño del problema, y agrupar funciones en categorías dependiendo de qué tan rápido crecen a medida que el tamaño del problema aumenta.


	Lo bueno de este tipo de comparaciones es que asegura una clasificación simple de los algoritmos. 

	Por ejemplo, si sé que el tiempo de ejecución del 'Algorigmo A' tiende a ser 'proporcional' al tamaño de la entrada, n, y el algoritmo B tiende a ser proporcional a n^2, entonces espero que A sea más rápido que B, al menos para valores grandes de n, aunque hay consideraciones.


	Orden de crecimiento:

		Supongamos que has analizado dos algoritmos y has expresado sus tiempos de ejecución en términos del tamaño de la entrada: 

			Al algoritmo A le toma 100n + 1 pasos resolver un problema con tamaño n; al algoritmo B le toma n^2+n+1 pasos.

		La siguiente tabla muestra el tiempo de ejecución de estos algoritmos para diferentes tamaños de problema:

		Tam. entrada 	Tiem ejec. A 	Tiem ejec. B
		10 				1.001 			111
		1.00			10.001 			10.101
		1.000 			100.001 		1.001.001
		2.0000			1.000.001 		100.010.001


		Cuando n = 10, el algoritmo A se ve bastante mal; toma casi 10 veces más que el algoritmo B.

		Pero para n = 100 son casi lo mismo, y para valores más grandes A es mucho mejor.

		La razón fundamental es que, para valores grandes de n, cualquier función que contiene el término n^2 crecerá más rápido que una función cuyo término principal es n. 

		El 'término principal' es el término con el exponente más alto.

		Para el algoritmo A, el término principal tiene un coeficiente grande, 100, que es el motivo por el cual B es mejor que A para n pequeño. 

		Pero a pesar de los coeficientes, siempre habrá algún valor de n donde an^2 > bn, para cualquier valor de a y b.

		El mismo argumento se aplica a los términos no principales.

		Incluso si el tiempo de ejecución del algoritmo A fuera n + 1000000, seguiría siendo mejor que el algoritmo B para n suficientemente grande.	


		En general, esperamos que un algoritmo con un 'término principal' más pequeño sea un mejor algoritmo para problemas grandes, pero para problemas más pequeños puede haber un 'punto de cruce' donde otro algoritmo es mejor. 

		La ubicación del 'punto de cruce' depende de los detalles de los algoritmos, las entradas y el hardware, por lo cual usualmente se ignora para propósitos de análisis algorítmico. 

		Pero eso no significa que puedes olvidarlo.

		Si dos algoritmos tienen el mismo término de orden principal, es difícil decir cuál es mejor; nuevamente, la respuesta depende de los detalles. 

		Entonces para análisis algorítmico, las 'funciones con el mismo término principal' se consideran equivalentes, incluso si tienen coeficientes diferentes.

		Un 'orden de crecimiento' es un conjunto de funciones cuyo comportamiento de crecimiento se considera equivalente. 

		Por ejemplo, 2n, 100n y n + 1 pertenecen al mismo orden de crecimiento, el cual se escribe O(n) en 'notación O grande' (en inglés, Big-Oh) y a menudo llamada 'lineal' porque cada función de dicho conjunto crece de manera lineal con n.

		Todas las funciones con término principal n^2 pertenecen a O(n^2): se llaman cuadráticas.


		La siguiente tabla muestra algunos de los órdenes de crecimiento que aparecen más comúnmente en el análisis algorítmico, en orden creciente de ineficiencia.

		Orden de crecimiento 	Nombre
		O(1)					Constante
		O(log_b n)				Log (cualquier base)
		O(n)					Lineal
		O(nlog_b n)	 			Linearítmica
		O(n^2) 					Cuadrática
		O(n^3) 					Cubíca
		O(c^n) 					Exp (cualquier c)


		Para los términos logarítmicos, la base del logarítmo no importa: cambiar las bases es equivalente a multiplicar por una constante, la cual no cambia el orden de crecimiento. 

		De igual manera, todas las funciones exponenciales pertenecen al mismo orden de crecimiento, independiente de la base del exponente. 

		Las funciones exponenciales crecen de manera muy rápida, por lo cual los algoritmos exponenciales solo son útiles para problemas pequeños.

		Los programadores que se preocupan del rendimiento a menudo encuentran este tipo de análisis difícil de tragar.

		Ellos tienen un punto: a veces 'los coeficientes y los términos no principales hacen una diferencia real'. 

		'A veces los detalles del hardware, el lenguaje de programación y las características de la entrada hacen una gran diferencia'. 

		Y para problemas pequeños, el orden de crecimiento es irrelevante.

		Pero si tienes en cuenta esas consideraciones, el análisis algorítmico es una herramienta útil. 

		Al menos 'para problemas grandes, el “mejor” algoritmo es generalmente mejor, y a veces es mucho mejor'. 

		La diferencia entre dos algoritmos con el mismo orden de crecimiento es generalmente un factor constante, ¡pero la diferencia entre un buen algoritmo y un mal algoritmo no tiene límites!


	Análisis de operaciones básicas de Python:

		En Python, la mayoría de las 'operaciones aritméticas son de tiempo constante'; la multiplicación generalmente toma más tiempo que la adición y sustracción, y la división toma aún más, pero estos tiempos de ejecución no dependen de la magnitud de los operandos. 

		Los 'enteros' muy grandes son una excepción: en ese caso el tiempo de ejecución aumenta con el número de dígitos. 

		Las 'operaciones de indexado —leer o escribir elementos en una secuencia o diccionario— también son de tiempo constante', independiente del tamaño de la estructura de datos.

		Un 'bucle for que recorre una secuencia o diccionario' es generalmente 'lineal', 'siempre y cuando todas las operaciones en el cuerpo del bucle sean de tiempo constante'.

		Por ejemplo, sumar los elementos de una lista es lineal:
			
			```
			total = 0
			for x in t:
				total += x

			```

		La función incorporada 'sum' también es 'lineal' porque hace lo mismo, pero 'tiende a ser más rápida porque es una implementación más eficiente'; en el lenguaje del análisis algorítmico, tiene un coeficiente principal más pequeño. 

		Como regla general, si el cuerpo de un bucle está en O (n^a) entonces el bucle completo está en O (n^a+1). 

		La excepción es cuando puedes mostrar que el bucle se interrumpe después de un número constante de iteraciones. 

		Si un bucle se ejecuta k veces independiente de n, entonces el bucle está en O (n^a), incluso para k grande. 

		Multiplicar por k no cambia el orden de crecimiento, ni tampoco dividir. 

		Entonces, si el cuerpo de un bucle está en O (n^a) y se ejecuta n/k veces, el bucle está en O (n^a+1), incluso para k grande. 

		La mayoría de las operaciones de 'cadena y de tupla son lineales', excepto 'indexar y len, que es de tiempo constante'. 

		Las funciones incorporadas 'min y max son lineales'. 

		El tiempo de ejecución de una operación de 'trozo es proporcional a la longitud de la salida, pero independiente del tamaño de la entrada'. 

		La 'concatenación de cadenas es lineal: el tiempo de ejecución depende de la suma de las longitudes de los operandos'.


		Todos los 'métodos de cadena son lineales', pero si las longitudes de las cadenas están 'acotadas por una constante' —por ejemplo, operaciones en caracteres individuales— se consideran de tiempo constante.

		El método de cadena join es lineal: el tiempo de ejecución depende de la longitud total de las cadenas.

		La mayoría de los métodos de lista son lineales, pero hay algunas excepciones:

			1. Agregar un elemento al final de una lista es de tiempo constante en promedio; cuando se queda sin espacio, ocasionalmente es copiada a una ubicación más grande, pero el tiempo total para n operaciones es O(n), por lo cual el tiempo promedio para cada operación es O(1).

			2. Eliminar un elemento del final de una lista es de tiempo constante.

			3. El ordenamiento es O (n log n) .


		La mayoría de las 'operaciones y métodos de diccionario son de tiempo constante', pero hay algunas excepciones:

			1. El tiempo de ejecución de 'update' es proporcional al tamaño del diccionario que se pasa como parámetro, no del diccionario que está siendo actualizado.

			2. 'keys, values e items' son de tiempo constante porque devuelven iteradores. 

			Pero si recorres un bucle con los iteradores, el bucle será lineal.

		El rendimiento de los diccionarios es uno de los milagros menores de las ciencias de la computación.


	Análisis de algoritmos de búsqueda:

		Una búsqueda es un algoritmo que toma una colección y un ítem objetivo y determina si el objetivo está en la colección, a menudo devolviendo el índice del objetivo. 

		El algoritmo de búsqueda más simple es la “búsqueda lineal”, que 'recorre los ítems de la colección en orden', deteniéndose si encuentra al objetivo. 

		En el 'peor de los casos tiene que recorrer toda la colección, por lo cual el tiempo de ejecución es lineal'. 

		El 'operador in' para secuencias utiliza una búsqueda lineal; los métodos de cadena como 'find y count' también. 

		'Si los elementos de la secuencia están en orden, puedes utilizar una búsqueda de bisección, que es O (log n)'. 

		La búsqueda de bisección es similar al algoritmo que podrías utilizar para buscar una palabra en un diccionario (un diccionario de papel, no la estructura de datos). 

		En lugar de comenzar del principio y revisar cada ítem en orden, comienzas con el ítem en el medio y verificas si la palabra que buscas viene antes o después. 

		Si viene antes, entonces buscas en la primera mitad de la secuencia. 

		De lo contrario, buscas la segunda mitad. 

		De cualquier manera, disminuyes el número de ítems restantes a la mitad. 

		Si la secuencia tiene 1.000.000 de ítems, tomará cerca de 20 pasos encontrar la palabra o concluir que no está. 

		Entonces, eso es cerca de 50.000 veces más rápido que una búsqueda lineal. 

		'La búsqueda de bisección puede ser mucho más rápida que una búsqueda lineal, pero requiere que la secuencia esté en orden, lo cual podría requerir trabajo extra'. 

		Hay otra estructura de datos, llamada 'tabla hash (en inglés, hashtable) que es incluso más rápida —puede hacer una búsqueda en tiempo constante— y no requiere que los ítems estén ordenados'. 

		Los diccionarios de Python se implementan utilizando tablas hash, por lo cual la mayoría de las operaciones de diccionario, incluyendo al operador in, son de tiempo constante.


	Tablas hash:

		Para explicar cómo funcionan las tablas hash y por qué su rendimiento es tan bueno, comienzo con una implementación simple de un mapa y gradualmente lo mejoro hasta que sea una tabla hash. 

		Yo utilizo Python para demostrar estas implementaciones, pero en la vida real no escribirías código como este en Python: ¡solo utilizarías un diccionario! Para el resto de este capítulo, tienes que imaginar que los diccionarios no existen y quieres implementar una estructura de datos que mapee de claves a valores. 

		Las operaciones que tienes que implementar son:

			add(k, v): 

				Agrega un nuevo ítem que mapea de una clave k a un valor v.

				Con un diccionario de Python, d, esta operación se escribe d[k] = v.

			get(k):

				Busca y devuelve el valor que corresponde a la clave k. 

				Con un diccionario de Python, d, esta operación se escribe d[k] o d.get(k).

		Por ahora, supongo que cada clave aparece una sola vez. 

		La implementación más simple de esta interfaz utiliza una lista de tuplas, donde cada tupla es un par clave-valor.

		```python

		class LinearMap:
			def __init__(self):
				self.items = []
			def add(self, k, v):
				self.items.append((k, v))
			def get(self, k):
				for key, val in self.items:
					if key == k:
						return val
				raise KeyError

		```

		add anexa una tupla clave-valor a la lista de ítems, lo cual toma tiempo constante. 

		get utiliza un bucle for para buscar la lista: encuentra la clave objetivo y devuelve el valor correspondiente; de lo contrario, ocurre un KeyError . Entonces, get es lineal. 

		Una alternativa es mantener la lista ordenada por clave.

		Entonces get podría utilizar una búsqueda de bisección, que es O (log n). 

		Pero insertar un nuevo ítem en el medio de una lista es lineal, por lo cual podría no ser la mejor opción. 

		Hay otras estructuras de datos que pueden implementar add y get en tiempo logarítmico, pero eso aún no es tan bueno como el tiempo constante, así que vamos a lo siguiente. 

		Una manera de mejorar LinearMap es separar la lista de pares clave-valor en listas más pequeñas. 

		Aquí hay una implementación llamada BetterMap, que es una lista de 100 LinearMaps. 

		Tal como veremos en un segundo, el orden de crecimiento para get aún es lineal, pero BetterMap es un paso en el camino hacia las tablas hash:

		```python

		class BetterMap:
			def __init__(self, n=100):
				self.maps = []
				for i in range(n):
					self.maps.append(LinearMap())
			def find_map(self, k):
				index = hash(k) % len(self.maps)
				return self.maps[index]
			def add(self, k, v):
				m = self.find_map(k)
				m.add(k, v)
			def get(self, k):
				m = self.find_map(k)
				return m.get(k)
		```	

		__init__ crea una lista de n LinearMaps.

		find_map es utilizado por add y get para averiguar en cuál mapa poner el nuevo ítem, o en cuál mapa buscar.

		find_map utiliza la función incorporada hash, que toma casi cualquier objeto de Python y devuelve un entero. 

		Una limitación de esta implementación es que solo funciona con claves hashables.

		Los tipos mutables como las listas y los diccionarios no son hashables. 

		Los objetos hashables que se consideran equivalentes devuelven el mismo valor hash, pero lo inverso no es necesariamente verdadero: dos objetos con valores diferentes pueden devolver el mismo valor hash. 

		find_map utiliza el operador de módulo para ajustar los valores hash en el rango entre 0 y len(self.maps), por lo cual el resultado es un índice legal en la lista. 

		Por supuesto, esto significa que muchos valores hash diferentes se ajustarán al mismo índice.

		Pero si la función hash distribuye las cosas de manera muy uniforme (que es para lo que están diseñadas las funciones hash), entonces esperamos n/100 ítems por cada LinearMap. 

		Dado que el tiempo de ejecución de LinearMap.get es proporcional al número de ítems, esperamos que BetterMap sea cerca de 100 veces más rápido que LinearMap.

		El orden de crecimiento es aún lineal, pero el coeficiente principal es más pequeño. 

		Eso es bueno, pero aún no es tan bueno como una tabla hash. 

		Aquí (finalmente) está la idea clave que hace que las tablas hash sean rápidas: si puedes mantener acotada la longitud máxima de los LinearMaps, LinearMap.get es de tiempo constante. 

		Todo lo que tienes que hacer es un seguimiento del número de ítems y cuando el número de ítems por cada LinearMap exceda un límite, cambiar el tamaño de la tabla hash añadiendo más LinearMaps.		

		```python

		class HashMap:
			def __init__(self):
				self.maps = BetterMap(2)
				self.num = 0
			def get(self, k):
				return self.maps.get(k)
			def add(self, k, v):
				if self.num == len(self.maps.maps):
					self.resize()
					self.maps.add(k, v)
					self.num += 1
			def resize(self):
				new_maps = BetterMap(self.num * 2)
					for m in self.maps.maps:
						for k, v in m.items:
							new_maps.add(k, v)
						self.maps = new_maps

		```

		__init__ crea un BetterMap e inicializa a num, que hace un seguimiento del número de ítems.

		get solo despacha a BetterMap.

		El trabajo real ocurre en add, que verifica el número de ítems y el tamaño del BetterMap: si son iguales, el número promedio de ítems por cada LinearMap es 1, entonces llama a resize.

		resize crea un nuevo BetterMap , dos veces más grande que el anterior, y luego “rehashea” los ítems desde el mapa antiguo hacia el nuevo.

		Rehashear es necesario porque al cambiar el número de LinearMaps cambia el denominador del operador de módulo en find_map.

		Eso significa que algunos objetos que solían hacer hash en el mismo LinearMap se dividirán (que es lo que queríamos, ¿verdad?). 

		El rehasheo es lineal, entonces resize es lineal, que podría parecer mal, dado que prometí que add sería de tiempo constante. 

		Pero recuerda que no tenemos que cambiar de tamaño cada vez, entonces add es generalmente de tiempo constante y solo ocasionalmente lineal. 

		La cantidad total de trabajo al ejecutar add n veces es proporcional a n, ¡entonces el tiempo promedio de cada add es de tiempo constante! Para ver cómo funciona esto, piensa en comenzar con un HashTable vacío y agregar una secuencia de ítems. 

		Comenzamos con 2 LinearMaps, entonces los 2 primeros añadidos son rápidos (no se requiere cambiar tamaño). Digamos que estos toman una unidad de trabajo cada uno. 

		El siguiente añadido requiere un cambio de tamaño, por lo cual tenemos que rehashear los primeros dos ítems (digamos que 2 unidades más de trabajo) y luego añadir el tercer ítem (una unidad más). 

		Añadir el siguiente ítem cuesta 1 unidad, entonces el total hasta ahora es de 6 unidades de trabajo para 4 ítems. 

		El siguiente add cuesta 5 unidades, pero los siguientes tres son solo una unidad cada uno, entonces el total es de 14 unidades para los primeros 8 añadidos. 

		El siguiente add cuesta 9 unidades, pero luego podemos añadir 7 más antes del siguiente cambio de tamaño, entonces el total es de 30 unidades para los primeros 16 añadidos. 

		Después de 32 añadidos, el costo total es de 62 unidades, y espero que comiences a ver el patrón. 

		Después de n añadidos, donde n es potencia de dos, el costo total es de 2n −2 unidades, entonces el trabajo promedio por cada añadido es un poco menos que dos unidades.

		Cuando n es una potencia de dos, ese es el mejor caso; para los otros valores de n el trabajo promedio es un poco más alto, pero eso no es importante. 

		Lo importante es que es O(1).

		La Figura B.1 muestra cómo funciona esto de manera gráfica. 

		Cada bloque representa una unidad de trabajo. 

		Las columnas muestran el trabajo total para cada añadido en orden de izquierda a derecha: los primeros dos adds cuestan 1 unidad cada uno, el tercero cuesta 3 unidades, etc. 

		El trabajo extra de rehashear aparece como una secuencia de torres cada vez más altas cuyo espacio entre ellas es cada vez mayor. 

		Ahora si derribas las torres, repartiendo el costo de cambiar de tamaño sobre todos los añadidos, puedes ver gráficamente que el costo total después de n añadidos es 2n − 2.

		Una característica importante de este algoritmo es que, cuando cambiamos el tamaño del HashTable, este crece de manera geométrica, es decir, multiplicamos el tamaño por una constante. 

		Si aumentas el tamaño de manera aritmética —añadiendo un número fijo cada vez— el tiempo promedio por cada add es lineal.



|| Bubble Sort
	
	Algoritmo de ordenación simple que itera repetidamente a través de la lista, compara elementos adyacentes y los intercambia si están en el orden incorrecto.

	Este proceso se repite hasta que la lista está ordenada. 

	Aunque es fácil de entender e implementar, no es eficiente para listas grandes debido a su complejidad temporal cuadrática


	Funcionamiento:

	    Recorre la lista múltiples veces.

	    En cada pasada, empuja el elemento más grande hacia su posición final.

	    El nombre "Bubble Sort" proviene de la forma en que los elementos más grandes "burbujearán" hacia la parte superior (final de la lista) con cada pasada.


	Paso a paso: 

		1. Inicialización:

		    Comenzamos desde el primer elemento de la lista.

		2. Comparación e Intercambio:

		    Comparamos cada par de elementos adyacentes.

		    Si el primer elemento es mayor que el segundo, los intercambiamos.

		3. Iteración:

		    Repetimos el proceso para todos los elementos de la lista.

		    Cada pasada completa coloca el siguiente elemento más grande en su lugar correcto.

		    Repetimos hasta que no se necesiten más intercambios.


	Implementación:

		```python

		def bubble_sort(arr):
		    n = len(arr)
		    for i in range(n):
		        swapped = False
		        for j in range(0, n-i-1):
		            if arr[j] > arr[j+1]:
		                arr[j], arr[j+1] = arr[j+1], arr[j]  # Intercambio
		                swapped = True
		        if not swapped:
		            break  # Si no hubo intercambios, la lista ya está ordenada
		    return arr

		```	

		Complejidad Temporal

	    Peor Caso: O(n^2):

	        Ocurre cuando la lista está ordenada en orden inverso.

	    Mejor Caso: O(n)

	        Ocurre cuando la lista ya está ordenada (con la optimización de detección de intercambio).

	    Caso Promedio: O(n^2)

	        Promedio de todas las posibles configuraciones de la lista


	Ventajas: 

		No requiere espacio adicional (ordenación en el lugar).


	Desventajas: 

		Ineficiente para listas grandes debido a su complejidad temporal cuadrática.
			
		Generalmente, hay algoritmos más eficientes disponibles para la mayoría de las aplicaciones prácticas.



|| Selection Sort	

	Es un algoritmo de ordenación simple y eficiente para listas pequeñas. 

	La idea principal es dividir la lista en dos partes: la sublista ordenada y la sublista desordenada. 

	Repetidamente encuentra el elemento mínimo (o máximo, dependiendo del orden) de la sublista desordenada y lo mueve al final de la sublista ordenada. 

	Este proceso se repite hasta que toda la lista está ordenada

	Es un buen algoritmo para aprender los fundamentos de la ordenación, especialmente debido a su simplicidad. 

	Sin embargo, debido a su ineficiencia para listas grandes, no es adecuado para aplicaciones prácticas donde se necesitan ordenar grandes volúmenes de datos. 

	Comprender Selection Sort proporciona una base para aprender algoritmos de ordenación más avanzados y eficientes, como Quick Sort y Merge Sort.


	Funcionamiento:

    	Encuentra el elemento mínimo en la parte desordenada de la lista.

    	Intercambia el elemento mínimo encontrado con el primer elemento de la parte desordenada.

    	Mueve el límite entre las partes ordenada y desordenada un elemento hacia la derecha.

    	Repite hasta que toda la lista está ordenada.


    Paso a Paso:

    	Inicialización:

    		Empezamos desde el primer elemento de la lista.

    	Selección del Elemento Mínimo:

    		Encuentra el elemento mínimo en la sublista desordenada.

    	Intercambio:

    		Intercambia el elemento mínimo encontrado con el primer elemento de la sublista desordenada.

		Repetición:

		    Repite el proceso para el resto de la lista, moviendo el límite de la sublista ordenada hacia la derecha en cada iteración.


	Implementación:

		def selection_sort(arr):
		    n = len(arr)
		    for i in range(n):
		        # Encuentra el elemento mínimo en la sublista arr[i:n]
		        min_idx = i
		        for j in range(i+1, n):
		            if arr[j] < arr[min_idx]:
		                min_idx = j
		        # Intercambia el elemento mínimo con el primer elemento de la sublista desordenada
		        arr[i], arr[min_idx] = arr[min_idx], arr[i]
		    return arr

		    ```


		Complejidad Temporal

		    Peor Caso: O(n^2)

		        Ocurre cuando la lista está ordenada en orden inverso.

		    Mejor Caso: O(n^2)

		        Incluso si la lista ya está ordenada, aún necesitamos comparar cada elemento.

		    Caso Promedio: O(n^2)

		        Promedio de todas las posibles configuraciones de la lista		    


		Complejidad Espacial

		    Espacio Adicional: O(1)

		        Solo necesita una cantidad constante de espacio adicional para las variables temporales, ya que la ordenación se realiza en el lugar (in-place).


	Ventajas: 

		Fácil de entender e implementar.

		Requiere una cantidad mínima de espacio adicional (in-place).


	Desventajas: 

		Ineficiente para listas grandes debido a su complejidad temporal cuadrática.

		No es estable (el orden relativo de elementos iguales puede cambiar).



|| Insertion Sort
	
	Algoritmo de ordenación simple e intuitivo que funciona de manera similar a cómo los humanos organizan cartas en una mano de naipes. 

	Es eficiente para listas pequeñas y generalmente más eficiente que Bubble Sort y Selection Sort en la práctica.


	Definición: 

		Insertion Sort es un algoritmo de ordenación que construye la lista ordenada uno a uno, insertando cada nuevo elemento en su posición correcta.


	Funcionamiento:

	    Divide la lista en una parte ordenada y una parte desordenada.

	    Toma elementos de la parte desordenada uno a uno y los inserta en la posición correcta dentro de la parte ordenada.

	    Repite hasta que toda la lista está ordenada.


	Paso a Paso:

		Inicialización:

		    Comienza con el segundo elemento (el primer elemento por sí solo está trivialmente ordenado).

		Inserción:

		    Toma el siguiente elemento de la parte desordenada.

		    Compara este elemento con los elementos de la parte ordenada y encuentra su posición correcta.

		    Inserta el elemento en su posición correcta desplazando los elementos mayores hacia la derecha.

		Repetición:

		    Repite el proceso hasta que toda la lista esté ordenada.			    


	Implementación:

		```python

		def insertion_sort(arr):
		    n = len(arr)
		    for i in range(1, n):
		        key = arr[i]
		        j = i - 1
		        # Mueve los elementos de arr[0..i-1], que son mayores que key, a una posición adelante de su posición actual
		        while j >= 0 and key < arr[j]:
		            arr[j + 1] = arr[j]
		            j -= 1
		        arr[j + 1] = key
		    return arr

		```

		Complejidad Temporal

		    Peor Caso: O(n^2)
		        Ocurre cuando la lista está ordenada en orden inverso.

		    Mejor Caso: O(n)
		        Ocurre cuando la lista ya está ordenada.

		    Caso Promedio: O(n^2)
		        
		        Promedio de todas las posibles configuraciones de la lista.


		Complejidad Espacial

		    Espacio Adicional: O(1)

		        Solo necesita una cantidad constante de espacio adicional para las variables temporales, ya que la ordenación se realiza en el lugar (in-place).


	Ventajas:

   		Fácil de entender e implementar.

    	Eficiente para listas pequeñas y casi ordenadas.

    	Ordena en el lugar (in-place).

    	Es estable (el orden relativo de elementos iguales se mantiene).


    Desventajas: 

		Ineficiente para listas grandes debido a su complejidad temporal cuadrática.    	



|| Merge Sort

	Algoritmo de ordenación eficiente y estable basado en el paradigma de divide y vencerás.

	Es uno de los algoritmos de ordenación más utilizados debido a su eficiencia y su capacidad para manejar listas grandes.

	
	Definición:

		Divide repetidamente una lista en mitades hasta que cada sublista tiene un solo elemento, luego combina (merge) las sublistas para producir listas ordenadas hasta obtener la lista final ordenada.


	Funcionamiento:

		Divide: 

			Divide la lista en dos mitades de manera recursiva hasta que cada sublista tiene un solo elemento.

		Conquista: 

			Ordena las dos mitades recursivamente.

		Combina: 

			Combina (merge) las dos mitades ordenadas en una sola lista ordenada.		

	Paso a Paso:

		1. División Recursiva:

		    Si la lista tiene más de un elemento, se divide en dos mitades.

		    La división continúa recursivamente hasta que las sublistas tienen un solo elemento.


		2. Combinación:

		    Comienza combinando las sublistas más pequeñas.

		    Durante la combinación, se comparan los elementos de las dos sublistas y se fusionan en una lista ordenada.

		    Este proceso se repite hasta que todas las sublistas se combinan en una lista ordenada. 	


	Implementación: 

		```python

		def merge_sort(arr):
		    if len(arr) > 1:
		        mid = len(arr) // 2
		        left_half = arr[:mid]
		        right_half = arr[mid:]

		        # Recursión en cada mitad
		        merge_sort(left_half)
		        merge_sort(right_half)

		        # Índices iniciales para sublistas left_half y right_half
		        i = j = k = 0

		        # Merging the sorted halves
		        while i < len(left_half) and j < len(right_half):
		            if left_half[i] < right_half[j]:
		                arr[k] = left_half[i]
		                i += 1
		            else:
		                arr[k] = right_half[j]
		                j += 1
		            k += 1

		        # Chequea si quedó algún elemento
		        while i < len(left_half):
		            arr[k] = left_half[i]
		            i += 1
		            k += 1

		        while j < len(right_half):
		            arr[k] = right_half[j]
		            j += 1
		            k += 1

		    return arr

		```

		Complejidad Temporal

    		Peor Caso: 

    			O(nlog⁡n)

    		Mejor Caso: 

    			O(nlog⁡n)
    		
    		Caso Promedio: 

    			O(nlog⁡n).


		Complejidad Espacial

		    Espacio Adicional: O(n)

		        Necesita espacio adicional proporcional al tamaño de la lista debido a las sublistas creadas durante la división y combinación


	Ventajas:

	    Eficiente con una complejidad temporal O(nlog⁡n) en todos los casos.
	    
	    Estable: preserva el orden relativo de los elementos iguales.

	    Funciona bien con listas grandes y datos almacenados en discos debido a su naturaleza de acceso secuencial.


	Desventajas:

	    Requiere espacio adicional proporcional al tamaño de la lista, lo que puede ser una limitación en sistemas con memoria limitada.

	    Más complicado de implementar que algoritmos más simples como Bubble Sort o Insertion Sort.



|| Quick Sort

	Uno de los algoritmos de ordenación más eficientes y ampliamente utilizados. 

	Se basa en el paradigma de divide y vencerás y es conocido por su eficiencia en promedio, aunque en el peor caso puede ser menos eficiente que otros algoritmos como Merge Sort.

	
	Definición:

		Selecciona un elemento como pivote y particiona la lista en dos sublistas: una con elementos menores al pivote y otra con elementos mayores al pivote. 

		Luego, ordena recursivamente las sublistas.


	Funcionamiento:

	    División: 

	    	Selecciona un pivote de la lista.

	    Partición: 

	    	Reorganiza los elementos de manera que todos los elementos menores que el pivote estén a su izquierda y todos los elementos mayores estén a su derecha.

	    Recursión: 

	    	Aplica recursivamente el mismo proceso a las sublistas izquierda y derecha	


	Paso a Paso:	

		1. Elección del Pivote:

			Elige un elemento de la lista como pivote. 

			Hay varias estrategias para elegir el pivote, como el primer elemento, el último elemento, un elemento al azar, o el mediano.

		Partición:

		    Reorganiza la lista de manera que los elementos menores que el pivote estén a su izquierda y los mayores a su derecha. 

		    El pivote está en su posición final.

		Recursión:

		    Aplica el proceso de forma recursiva a las sublistas izquierda y derecha hasta que la lista esté completamente orden.


	Implementación:
		
		Usando el último elemento como pivote.

		```python

		def partition(arr, low, high):
		    pivot = arr[high]
		    i = low - 1  # Índice del elemento más pequeño
		    for j in range(low, high):
		        if arr[j] <= pivot:
		            i += 1
		            arr[i], arr[j] = arr[j], arr[i]  # Intercambio
		    arr[i + 1], arr[high] = arr[high], arr[i + 1]  # Intercambio el pivote
		    return i + 1

		def quick_sort(arr, low, high):
		    if low < high:
		        pi = partition(arr, low, high)
		        quick_sort(arr, low, pi - 1)
		        quick_sort(arr, pi + 1, high)
		    return arr

		# Ejemplo de uso
		arr = [10, 7, 8, 9, 1, 5]
		n = len(arr)
		sorted_arr = quick_sort(arr, 0, n - 1)
		print(f"Lista ordenada: {sorted_arr}")

		```

		Complejidad Temporal:

		    Peor Caso: O(n^2)

		        Ocurre cuando el pivote elegido es siempre el más grande o el más pequeño elemento.

		    Mejor Caso: O(nlog⁡n)

		        Ocurre cuando el pivote divide la lista en dos mitades casi iguales en cada iteración.

		    Caso Promedio: O(nlog⁡n)

		        Generalmente, debido a la aleatoriedad del pivote.


		Complejidad Espacial

		    Espacio Adicional: O(log⁡n)

		        En la mayoría de las implementaciones, debido a la pila de llamadas recursivas.


	Ventajas

		Generalmente, es más rápido en promedio que otros algoritmos O(nlog⁡n) debido a su naturaleza de acceso en memoria.

	    Ordena en el lugar (in-place).

	    Es ampliamente utilizado y bien estudiado, con muchas optimizaciones disponibles.


	Desventajas:

	    El peor caso es O(n^2), aunque esto puede ser mitigado con buenas estrategias para la elección del pivote (como elegir uno al azar).

	    No es estable (el orden relativo de elementos iguales puede cambiar).

	    La implementación recursiva puede causar un desbordamiento de pila para listas muy gran grandes.



|| Algoritmos y Estructuras de Datos Avanzadas

	
	1. Recorridos de Grafos:

    	BFS (Breadth-First Search).
    	
    	DFS (Depth-First Search).	


    2. Estructuras de Datos Avanzadas:

    	Árboles binarios.
    	
    	Árboles AVL.
    	
    	Heaps.


    Algoritmos de Recorrido:

    	Son técnicas utilizadas para visitar todos los nodos en una estructura de datos, típicamente grafos o árboles. 

    	Estos algoritmos son fundamentales en ciencias de la computación y tienen aplicaciones en diversas áreas, como la búsqueda de información, la optimización de rutas, y la inteligencia artificial.


    	1. Recorrido en Árboles:

    		1. Recorrido en Profundidad (DFS - Depth First Search):

				El recorrido en profundidad es un algoritmo que visita todos los nodos de un árbol (o un grafo) explorando tan lejos como sea posible a lo largo de cada rama antes de retroceder.


			Tipos de Recorridos DFS en Árboles:

			    Preorden (Preorder):
			        
			        Visita la raíz.

			        Recorre el subárbol izquierdo.

			        Recorre el subárbol derecho.

			    Inorden (Inorder):

			        Recorre el subárbol izquierdo.

			        Visita la raíz.
			        Recorre el subárbol derecho.

			    Postorden (Postorder):

			        Recorre el subárbol izquierdo.

			        Recorre el subárbol derecho.

			        Visita la raíz


			Ejemplo de Recorridos DFS:

				```
					1
				   / \
				  2   3
				 / \
				4   5

				```

				Preorden: 1, 2, 4, 5, 3

    			Inorden: 4, 2, 5, 1, 3
    			
    			Postorden: 4, 5, 2, 3, 1


    		2. Recorrido en Anchura (BFS - Breadth First Search)

				El recorrido en anchura visita todos los nodos de un árbol (o un grafo) nivel por nivel, es decir, primero visita todos los nodos en el nivel actual antes de proceder a los nodos en el siguiente nivel.

				```
				    1
				   / \
				  2   3
				 / \
				4   5

				```

				BFS: 1, 2, 3, 4, 5


		2. Recorrido en Grafos
			
			Recorrido en Profundidad (DFS)

				El DFS en grafos funciona de manera similar al DFS en árboles. 

				Utiliza una pila (puede ser la pila de llamadas del sistema en una implementación recursiva) para recordar los vértices que debe visitar.			


			Recorrido en Anchura (BFS)

				El BFS en grafos utiliza una cola para recordar los vértices que debe visitar.


			Recorrido en Anchura (BFS)

				El BFS en grafos utiliza una cola para recordar los vértices que debe visitar.


			DFS vs BFS:

				DFS:

    				Puede ser implementado de manera recursiva o con una pila.

    				Es útil para explorar todos los caminos en laberintos y problemas similares.

   					Puede quedar atrapado en ciclos infinitos si no se manejan correctamente los grafos cíclicos.


   				BFS:

    				Utiliza una cola y es menos propenso a quedarse atrapado en ciclos.

    				Encuentra el camino más corto en grafos no ponderados.

 					Requiere más memoria que DFS, ya que almacena todos los nodos en el nivel actual.


			Los algoritmos de recorrido, tanto DFS como BFS, son herramientas fundamentales para la exploración y manipulación de estructuras de datos como árboles y grafos.

			Cada uno tiene sus propias ventajas y aplicaciones ideales, dependiendo de la estructura de datos y del problema específico a resolver.



|| DFS
	
	Recorrido en Profundidad (Depth First Search) es algoritmo fundamental para recorrer o buscar en estructuras de datos como árboles y grafos. 

	DFS explora tan lejos como sea posible a lo largo de cada rama antes de retroceder


	Estrategia de Exploración:

	    El algoritmo comienza en un nodo inicial y explora cada uno de sus vecinos antes de retroceder.

	    Esto implica ir hacia el fondo de una rama del grafo antes de intentar otros caminos.


	Estructura de Datos Utilizada:

	    DFS puede implementarse de forma recursiva utilizando la pila de llamadas del sistema.

	    También puede implementarse de manera iterativa usando una pila explícita.


	Visitas y Retrocesos:

	    Un nodo se marca como visitado cuando se llega a él por primera vez.

	    El algoritmo retrocede cuando no hay más nodos adyacentes no visitados.



	Implementación Recursiva:

		```python

		def dfs_recursive(graph, start, visited=None):
		    if visited is None:
		        visited = set()
		    visited.add(start)
		    print(start)  # O almacenar en una lista para otros usos
		    for neighbor in graph[start]:
		        if neighbor not in visited:
		            dfs_recursive(graph, neighbor, visited)
		    return visited

		# Ejemplo de uso
		graph = {
		    'A': ['B', 'C'],
		    'B': ['A', 'D', 'E'],
		    'C': ['A', 'F'],
		    'D': ['B'],
		    'E': ['B', 'F'],
		    'F': ['C', 'E']
		}

		dfs_recursive(graph, 'A')

		```

	
	Implementación Iterativa:		

		```python

		def dfs_iterative(graph, start):
		    visited = set()
		    stack = [start]
		    while stack:
		        vertex = stack.pop()
		        if vertex not in visited:
		            visited.add(vertex)
		            print(vertex)  # O almacenar en una lista para otros usos
		            stack.extend([neighbor for neighbor in graph[vertex] if neighbor not in visited])
		    return visited

		# Ejemplo de uso
		dfs_iterative(graph, 'A')

		```


	Funcionamiento:

		Considerando el siguiente grafo.


		```
		    A
		   / \
		  B   C
		 / \   \
		D   E   F
		 \ /   /
		  F - E

		```

		DFS Recursivo desde 'A':

		    Comienza en 'A', marca 'A' como visitado.

		    Visita 'B', marca 'B' como visitado.

		    Visita 'D', marca 'D' como visitado.

		    'D' tiene un vecino 'F' no visitado, visita 'F', marca 'F' como visitado.

		    Retrocede a 'D', luego a 'B'.

		    Visita 'E', marca 'E' como visitado.

		    'E' tiene un vecino 'F' ya visitado, retrocede a 'B', luego a 'A'.

		    Visita 'C', marca 'C' como visitado.

		    'C' tiene un vecino 'F' ya visitado.
	
		
		El orden de visita será: A, B, D, F, E, C.


	Complejidad de DFS

	    Complejidad Temporal:
	        
	        En un grafo representado por listas de adyacencia, la complejidad temporal de DFS es O(V+E), donde V es el número de vértices y E es el número de aristas.


	    Complejidad Espacial:
	        
	        En el caso de la implementación recursiva, la complejidad espacial es O(V) debido a la pila de llamadas del sistema.


        En la implementación iterativa, la complejidad espacial también es O(V) debido a la pila explícita utilizada.


    Aplicaciones de de DFS

	    Detección de Ciclos:

	        DFS puede ser utilizado para detectar ciclos en un grafo.

	    Componentes Conectados:

	        Ayuda a encontrar componentes conectados en grafos no dirigidos.

	    Orden Topológico:

	        Se utiliza en grafos dirigidos acíclicos (DAG) para realizar un orden topológico.

	    Resolución de Laberintos y Puzzles:

	        Útil para resolver problemas de búsqueda exhaustiva, como laberintos y puzzles que requieren explorar todos los caminos posibles.


	La implementación de DFS puede ser sencilla, pero su capacidad para resolver problemas complejos y su eficiencia lo convierten en una herramienta esencial en ciencias de la computación.



|| BFS
	
	Recorrido en Anchura (Breadth First Search) es un algoritmo utilizado para recorrer o buscar en estructuras de datos como grafos y árboles. 

	A diferencia del DFS, el BFS explora todos los nodos en el nivel actual antes de moverse al siguiente nivel, lo que lo hace particularmente útil para encontrar el camino más corto en grafos no ponderados .


	Estrategia de Exploración:

	    Comienza en un nodo inicial y explora todos los vecinos en el nivel actual antes de pasar a los vecinos del siguiente nivel.


	Estructura de Datos Utilizada:

	    Utiliza una cola (FIFO) para recordar los nodos que debe visitar.


	Visitas Nivel por Nivel:

	    Los nodos se visitan nivel por nivel, lo que garantiza que se encuentran los caminos más cortos en grafos no ponderados.
	

	Implementación:

		Usando un cola. 

		```python

		from collections import deque

		def bfs(graph, start):
		    visited = set()
		    queue = deque([start])
		    visited.add(start)
		    while queue:
		        vertex = queue.popleft()
		        print(vertex)  # O almacenar en una lista para otros usos
		        for neighbor in graph[vertex]:
		            if neighbor not in visited:
		                visited.add(neighbor)
		                queue.append(neighbor)
		    return visited

		# Ejemplo de uso
		graph = {
		    'A': ['B', 'C'],
		    'B': ['A', 'D', 'E'],
		    'C': ['A', 'F'],
		    'D': ['B'],
		    'E': ['B', 'F'],
		    'F': ['C', 'E']
		}

		bfs(graph, 'A')

		```


	Funcionamiento:

		```
		    A
		   / \
		  B   C
		 / \   \
		D   E   F
		 \ /   /
		  F - E

		```

		BFS desde 'A':

		    Comienza en 'A', marca 'A' como visitado.

		    Coloca 'A' en la cola.

		    Desencola 'A' y visita sus vecinos: 'B' y 'C'.

		    Marca 'B' y 'C' como visitados y los coloca en la cola.

		    Desencola 'B' y visita sus vecinos: 'D' y 'E'.

		    Marca 'D' y 'E' como visitados y los coloca en la cola.

		    Desencola 'C' y visita su vecino: 'F'.

		    Marca 'F' como visitado y lo coloca en la cola.

		    Desencola 'D'. 

		    Sus vecinos ya están visitados, no hace nada.

		    Desencola 'E'. 

		    Sus vecinos ya están visitados, no hace nada.

		    Desencola 'F'. 

		    Sus vecinos ya están visitados, no hace nada.

		El orden de visita será: A, B, C, D, E, F.


	Complejidad de BFS

	    Complejidad Temporal:

	        En un grafo representado por listas de adyacencia, la complejidad temporal de BFS es O(V+E), donde VV es el número de vértices y EE es el número de aristas.

	    Complejidad Espacial:

	        La complejidad espacial es O(V), ya que se debe almacenar la cola y el conjunto de nodos visitados.


	Aplicaciones de BFS

	    Encontrar el Camino Más Corto:

	        BFS es ideal para encontrar el camino más corto en grafos no ponderados.

	    Nivel de Nodos:

	        Determina el nivel o la profundidad de los nodos en un grafo.

	    Conectividad:

	        Puede ser usado para verificar si un grafo no dirigido es conexo.

	    Algoritmos de Flujo de Red:

	        BFS se utiliza en el algoritmo de Edmonds-Karp para encontrar el flujo máximo en una red de flujo.

	    Búsqueda de Palabra en Tablero:

	        Utilizado en problemas como la búsqueda de palabras en un tablero de letras (e.g., Boggle).


	DFS vs BFS:

		BFS:

		    Explora por niveles.

		    Encuentra el camino más corto en grafos no ponderados.

		    Puede requerir más memoria, ya que mantiene todos los nodos en el nivel actual en la cola.

		DFS:

		    Explora tan lejos como sea posible antes de retroceder.

		    No garantiza encontrar el camino más corto.

		    Generalmente requiere menos memoria que BFS, pero puede quedar atrapado en ciclos si no se manejan correctamente.



|| Teoría de Grafos
	
	Área de las matemáticas y la informática que estudia los grafos, que son estructuras formadas por vértices (nodos) y aristas (enlaces) que conectan pares de vértices.


	Elementos:

		Vértices (Nodos):

		    Representan objetos o entidades en un grafo.

		    Se denotan comúnmente como V o N.

		Aristas (Enlaces):

		    Representan las conexiones entre los vértices.

		    Se denotan comúnmente como E.


	Tipos de Grafos:

		1. Grafo Dirigido (Digrafo):

		    Las aristas tienen una dirección, es decir, van de un vértice a otro.

		    Se representan como pares ordenados (u,v).


		2. Grafo No Dirigido:

		    Las aristas no tienen dirección.

		    Se representan como conjuntos no ordenados {u,v}.


		3. Grafo Ponderado:

		    Las aristas tienen asociados valores o pesos que representan el costo, la distancia, o alguna otra medida.


		4. Grafo No Ponderado:

		    Las aristas no tienen pesos asociados.


		5. Grafo Conexo:

		    Existe un camino entre cualquier par de vértices en el grafo.


		6. Grafo Desconexo:

		    No todos los vértices están conectados por un camino.


		7. Grafo Bipartito:

		    Los vértices se pueden dividir en dos conjuntos disjuntos, donde no hay aristas entre vértices del mismo conjunto.


		8. Grafo Completo:

		    Cada par de vértices está conectado por una arista.		


	Propiedades: 

		Grado de un Vértice:

		    Número de aristas incidentes en un vértice. 

		    En un grafo dirigido, se distingue entre grado de entrada y grado de salida.

		Camino:

		    Secuencia de aristas que conectan un conjunto de vértices.

		Ciclo:

		    Un camino que comienza y termina en el mismo vértice y no repite aristas ni vértices (excepto el inicio y el final).

		Distancia:

		    Número mínimo de aristas que hay que recorrer para ir de un vértice a otro.


	Problemas Clásicos:

		Camino Más Corto:

		    Encontrar la ruta de menor costo entre dos vértices.

		    Algoritmos: Dijkstra, Bellman-Ford.


		Árbol de Expansión Mínima:

		    Encontrar un subconjunto de aristas que conecten todos los vértices con el peso total mínimo.

		    Algoritmos: Kruskal, Prim.


		Coloración de Grafos:

		    Asignar colores a los vértices de un grafo de tal manera que no haya dos vértices adyacentes del mismo color.


		Flujo Máximo:

		    Encontrar la máxima cantidad de flujo que se puede enviar a través de una red de flujo desde una fuente a un sumidero.
		    Algoritmos: Ford-Fulkerson, Edmonds-Karp.


		Emparejamiento en Grafos Bipartitos:

		    Emparejar los vértices de dos conjuntos de tal manera que el número de emparejamientos sea máximo.

		    Algoritmos: Hopcroft-Karp.


	Algoritmos de Recorrido en Grafos

	    Búsqueda en Profundidad (DFS):

	        Explora lo más profundo posible a partir de cada vértice antes de retroceder.

	        Utilizado para detectar ciclos, ordenar topológicamente, y encontrar componentes fuertemente conexos.


	    Búsqueda en Anchura (BFS):

	        Explora todos los vértices en el nivel actual antes de moverse al siguiente nivel.

	        Utilizado para encontrar el camino más corto en grafos no ponderados y en algoritmos de flujo.


	Representaciones de Grafos

	    Lista de Adyacencia:

	        Un array o lista donde cada posición contiene una lista de los vértices adyacentes a un vértice específico.

	        Eficiente en términos de espacio para grafos dispersos.


	    Matriz de Adyacencia:

	        Una matriz n×n, donde n es el número de vértices, y el valor en la posición (i,j) indica si existe una arista entre los vértices i y j.

	        Eficiente para grafos densos.


	Aplicaciones de la Teoría de Grafos

	    Redes de Computadoras:

	        Modelar la conectividad y las rutas en redes de computadoras.

	    Redes Sociales:

	        Representar relaciones y conexiones entre personas.

	    Sistemas de Transporte:

	        Optimizar rutas y planificar caminos en sistemas de transporte.

	    Biología Computacional:

	        Modelar redes de interacción genética y análisis de estructuras moleculares.

	    Inteligencia Artificial:

	        Resolver problemas de planificación y búsqueda.


	Ejemplo:

		Implentación de un grafo y un algoritmo de recorrido en profundidad (DFS).

		```python

		class Grafo:
		    def __init__(self):
		        self.grafo = {}

		    def agregar_vertice(self, vertice):
		        if vertice not in self.grafo:
		            self.grafo[vertice] = []

		    def agregar_arista(self, vertice1, vertice2):
		        if vertice1 in self.grafo and vertice2 in self.grafo:
		            self.grafo[vertice1].append(vertice2)
		            self.grafo[vertice2].append(vertice1)  # Para un grafo no dirigido

		    def dfs(self, inicio, visitados=None):
		        if visitados is None:
		            visitados = set()
		        visitados.add(inicio)
		        print(inicio, end=' ')
		        for vecino in self.grafo[inicio]:
		            if vecino not in visitados:
		                self.dfs(vecino, visitados)

		# Ejemplo de uso
		g = Grafo()
		g.agregar_vertice('A')
		g.agregar_vertice('B')
		g.agregar_vertice('C')
		g.agregar_arista('A', 'B')
		g.agregar_arista('A', 'C')
		g.agregar_arista('B', 'C')

		print("Recorrido DFS:")
		g.dfs('A')

		```



|| Árbol 
	
	Es una estructura de datos jerárquica que consiste en nodos conectados por aristas, y es un caso especial de grafo.


	Conceptos:

		Nodo: 	

			Un elemento del árbol que contiene un valor o dato.

		Arista (Edge): 

			Conexión entre dos nodos.

		Raíz (Root): 

			El nodo superior de un árbol, que no tiene padres.

		Hijos (Children): 

			Nodos directamente conectados a un nodo específico (su padre).

		Padre (Parent): 

			El nodo que tiene una arista dirigida a uno de sus hijos.

		Hoja (Leaf): 

			Un nodo que no tiene hijos.

		Subárbol (Subtree): 

			Un nodo y todos sus descendientes forman un subárbol.

		Nivel (Level): 

			La distancia desde la raíz a un nodo específico. 

			La raíz está en el nivel 0, sus hijos están en el nivel 1, y así sucesivamente.

		Altura (Height): 

			La longitud del camino más largo desde un nodo hasta una hoja. 

			La altura de un árbol es la altura de la raíz.

		Profundidad (Depth): 

			La longitud del camino desde la raíz hasta un nodo específico. 

			La profundidad de la raíz es 0.


	Propiedades de los Árboles

	    Acríclico: 

	    	Un árbol no tiene ciclos.

	    Conexión: 

	    	Un árbol es un grafo conectado, es decir, hay un camino entre cualquier par de nodos.

	    Nodos y Aristas: 

	    	Un árbol con n nodos siempre tiene n−1 aristas.

	    Unicidad de Caminos: 

	    	Existe exactamente un camino entre cualquier par de nodos en un árbol.


	Tipos de Árboles

	    1. Árbol Binario: 

	    	Cada nodo tiene como máximo dos hijos.

	        Árbol Binario Completo:

	        	Todos los niveles están completamente llenos excepto posiblemente el último, que está lleno de izquierda a derecha.

	        Árbol Binario Perfecto:

	        	Todos los niveles están completamente llenos.

	        Árbol Binario de Búsqueda (BST): 

	        	Un árbol binario donde cada nodo tiene un valor mayor que todos los valores en su subárbol izquierdo y menor que todos los valores en su subárbol derecho.


	    2. Árbol AVL: 

	    	Un árbol binario de búsqueda autobalanceado donde las alturas de los dos subárboles de un nodo difieren en no más de uno.

		
		3. Árbol Rojo-Negro: 

			Un árbol binario de búsqueda autobalanceado con reglas adicionales para asegurar un equilibrio balanceado.


		4. Árbol B: 

			Un árbol autoajustable utilizado en bases de datos y sistemas de archivos.


	Operaciones de Árboles: 

		1. Inserción: 

			Agregar un nuevo nodo al árbol en una posición específica según las reglas del árbol.

		2. Eliminación: 

			Quitar un nodo del árbol y reorganizarlo para mantener las propiedades del árbol.

		3. Búsqueda: 

			Encontrar un nodo con un valor específico.

		4. Recorrido (Traversal):

		    Preorden (Preorder):

		    	Visitar la raíz, luego el subárbol izquierdo y finalmente el subárbol derecho.

		    Inorden (Inorder):

		    	Visitar el subárbol izquierdo, luego la raíz y finalmente el subárbol derecho.

		    Postorden (Postorder):

		    	Visitar el subárbol izquierdo, luego el subárbol derecho y finalmente la raíz.

		    Por Nivel (Level Order):

		   		Visitar los nodos nivel por nivel, de arriba hacia abajo.


	Implementación: 

		```python

		class Node:
		    def __init__(self, key):
		        self.left = None
		        self.right = None
		        self.val = key

		# Recorridos
		def inorder(root):
		    if root:
		        inorder(root.left)
		        print(root.val, end=' ')
		        inorder(root.right)

		def preorder(root):
		    if root:
		        print(root.val, end=' ')
		        preorder(root.left)
		        preorder(root.right)

		def postorder(root):
		    if root:
		        postorder(root.left)
		        postorder(root.right)
		        print(root.val, end=' ')

		# Ejemplo de uso
		root = Node(1)
		root.left = Node(2)
		root.right = Node(3)
		root.left.left = Node(4)
		root.left.right = Node(5)

		print("Recorrido Inorden:")
		inorder(root)

		print("\nRecorrido Preorden:")
		preorder(root)

		print("\nRecorrido Postorden:")
		postorder(root)

		```

	
	Aplicaciones:

		Búsqueda y Ordenación: 

			Los árboles binarios de búsqueda permiten búsquedas rápidas, inserciones y eliminaciones.
		
		Estructuras de Datos:

			Utilizados en implementaciones de colas de prioridad, montículos (heaps), y otros ADTs (Abstract Data Types).

		Bases de Datos: 

			Los árboles B y B+ se utilizan para la indexación y recuperación eficiente de datos.

		Compresión de Datos: 

			Los árboles de Huffman se utilizan en algoritmos de compresión como el ZIP.



|| Árbol Binario

	Estructura de datos jerárquica en la que cada nodo tiene, como máximo, dos hijos: el hijo izquierdo y el hijo derecho. 

	Los árboles binarios son fundamentales en informática y se utilizan en una variedad de aplicaciones, como la búsqueda y la ordenación de datos.


	Conceptos: 

		Nodo: 

			La unidad básica de un árbol, que contiene un valor y referencias a sus hijos.

		Raíz (Root): 

			El nodo superior del árbol.

		Hijos (Children): 

			Los nodos directamente conectados a un nodo específico.

		Padre (Parent): 

			El nodo que tiene un enlace a uno de sus hijos.

		Hoja (Leaf): 

			Un nodo que no tiene hijos.

		Subárbol (Subtree): 

			Un nodo y todos sus descendientes.

		Altura (Height): 

			La longitud del camino más largo desde la raíz hasta una hoja.

		Profundidad (Depth): 

			La longitud del camino desde la raíz hasta un nodo específico.


	Implementación: 

		```python

		class Node:
		    def __init__(self, key):
		        self.left = None
		        self.right = None
		        self.val = key

		class BinaryTree:
		    def __init__(self):
		        self.root = None

		    def insert(self, key):
		        if self.root is None:
		            self.root = Node(key)
		        else:
		            self._insert(self.root, key)

		    def _insert(self, node, key):
		        if key < node.val:
		            if node.left is None:
		                node.left = Node(key)
		            else:
		                self._insert(node.left, key)
		        else:
		            if node.right is None:
		                node.right = Node(key)
		            else:
		                self._insert(node.right, key)

		    def inorder(self, node):
		        if node:
		            self.inorder(node.left)
		            print(node.val, end=' ')
		            self.inorder(node.right)

		    def preorder(self, node):
		        if node:
		            print(node.val, end=' ')
		            self.preorder(node.left)
		            self.preorder(node.right)

		    def postorder(self, node):
		        if node:
		            self.postorder(node.left)
		            self.postorder(node.right)
		            print(node.val, end=' ')

		# Ejemplo de uso
		tree = BinaryTree()
		tree.insert(10)
		tree.insert(5)
		tree.insert(20)
		tree.insert(3)
		tree.insert(7)

		print("Recorrido Inorden:")
		tree.inorder(tree.root)
		print("\nRecorrido Preorden:")
		tree.preorder(tree.root)
		print("\nRecorrido Postorden:")
		tree.postorder(tree.root)

		```


	Aplicaciones: 

	    Árbol Binario de Búsqueda (BST): 

	    	Permite operaciones eficientes de búsqueda, inserción y eliminación.

	    Árboles AVL y Rojo-Negro:

	    	Tipos de árboles binarios balanceados utilizados para mantener operaciones balanceadas en BST.

	    Árboles de Expresión:

	    	Utilizados en análisis sintáctico de expresiones matemáticas.

	    Estructuras de Archivos: 

	    	Los sistemas de archivos utilizan árboles binarios para organizar y buscar archivos de manera eficiente.

	    Compresión de Datos: 

	    	Los árboles de Huffman se utilizan en algoritmos de compresión de datos.



|| Árbol AVL

	Es un tipo de árbol binario de búsqueda (BST) que se autobalancea para asegurar que las operaciones de búsqueda, inserción y eliminación sean eficientes. 

	Fue el primer árbol binario de búsqueda autobalanceado, introducido por los matemáticos Adelson-Velsky y Landis en 1962.


	Balanceado por Altura:

	    Para cualquier nodo en un árbol AVL, la diferencia en la altura de los subárboles izquierdo y derecho (también conocida como el factor de equilibrio o balance factor) es como máximo 1.

	    Factor de equilibrio = Altura del subárbol izquierdo - Altura del subárbol derecho.


	Operaciones en Tiempo Logarítmico:

	    Las operaciones de búsqueda, inserción y eliminación tienen una complejidad temporal de O(log⁡n), donde n es el número de nodos en el árbol, debido a la propiedad de balanceo.


	Rotaciones en un Árbol AVL:

		Para mantener el árbol balanceado, se utilizan rotaciones cuando se inserta o elimina un nodo que provoca un desbalance. 

		Hay cuatro tipos de rotaciones:

		    1. Rotación Simple a la Derecha (Right Rotation):

		        Se usa cuando se inserta un nodo en el subárbol izquierdo del hijo izquierdo.

		        También conocida como rotación LL.

		    2. Rotación Simple a la Izquierda (Left Rotation):

		        Se usa cuando se inserta un nodo en el subárbol derecho del hijo derecho.

		        También conocida como rotación RR.

		    3. Rotación Doble a la Derecha (Left-Right Rotation):

		        Se usa cuando se inserta un nodo en el subárbol derecho del hijo izquierdo.

		        También conocida como rotación LR.

		    4. Rotación Doble a la Izquierda (Right-Left Rotation):

		        Se usa cuando se inserta un nodo en el subárbol izquierdo del hijo derecho.

		        También conocida como rotación RL.


	Implementación:

		```python

		class TreeNode:
		    def __init__(self, key):
		        self.key = key
		        self.left = None
		        self.right = None
		        self.height = 1

		class AVLTree:
		    def insert(self, root, key):
		        if not root:
		            return TreeNode(key)
		        elif key < root.key:
		            root.left = self.insert(root.left, key)
		        else:
		            root.right = self.insert(root.right, key)

		        root.height = 1 + max(self.get_height(root.left), self.get_height(root.right))
		        balance = self.get_balance(root)

		        # Rotación LL
		        if balance > 1 and key < root.left.key:
		            return self.right_rotate(root)
		        # Rotación RR
		        if balance < -1 and key > root.right.key:
		            return self.left_rotate(root)
		        # Rotación LR
		        if balance > 1 and key > root.left.key:
		            root.left = self.left_rotate(root.left)
		            return self.right_rotate(root)
		        # Rotación RL
		        if balance < -1 and key < root.right.key:
		            root.right = self.right_rotate(root.right)
		            return self.left_rotate(root)

		        return root

		    def left_rotate(self, z):
		        y = z.right
		        T2 = y.left
		        y.left = z
		        z.right = T2
		        z.height = 1 + max(self.get_height(z.left), self.get_height(z.right))
		        y.height = 1 + max(self.get_height(y.left), self.get_height(y.right))
		        return y

		    def right_rotate(self, z):
		        y = z.left
		        T3 = y.right
		        y.right = z
		        z.left = T3
		        z.height = 1 + max(self.get_height(z.left), self.get_height(z.right))
		        y.height = 1 + max(self.get_height(y.left), self.get_height(y.right))
		        return y

		    def get_height(self, root):
		        if not root:
		            return 0
		        return root.height

		    def get_balance(self, root):
		        if not root:
		            return 0
		        return self.get_height(root.left) - self.get_height(root.right)

		    def inorder(self, root):
		        if root:
		            self.inorder(root.left)
		            print(root.key, end=' ')
		            self.inorder(root.right)

		# Ejemplo de uso
		tree = AVLTree()
		root = None
		keys = [10, 20, 30, 40, 50, 25]

		for key in keys:
		    root = tree.insert(root, key)

		print("Recorrido Inorden del árbol AVL:")
		tree.inorder(root)

		```


	Ventajas de los Árboles AVL:

		Eficiencia:

		    Mantienen la altura del árbol como O(log⁡n), asegurando búsquedas, inserciones y eliminaciones eficientes.

		Balanceo Automático:

		    El árbol se autobalancea después de cada inserción y eliminación, lo que minimiza la necesidad de intervención manual para mantener el balance.


	Aplicaciones:

		Bases de Datos:

		    Utilizados en la implementación de índices para asegurar búsquedas rápidas.

		Sistemas de Archivos:

		    Utilizados en la gestión de estructuras de directorios y archivos.

		Aplicaciones en Tiempo Real:

		    Beneficiosos en sistemas donde las operaciones rápidas y predecibles son críticas.	



|| Heap

	Estructura de datos basada en un árbol que cumple con la propiedad del heap, que puede ser un Heap Máximo (Max-Heap) o un Heap Mínimo (Min-Heap). 

	Los heaps se utilizan principalmente para implementar colas de prioridad y para algoritmos de ordenación como el Heapsort.


	Propiedad del Heap:

	    Heap Máximo (Max-Heap): 

	    	En un Max-Heap, para cualquier nodo i que no sea la raíz, el valor de i es menor o igual que el valor de su padre.

	    	Esto significa que el valor máximo está en la raíz.

	    Heap Mínimo (Min-Heap): 

	    	En un Min-Heap, para cualquier nodo i que no sea la raíz, el valor de i es mayor o igual que el valor de su padre.

	    	Esto significa que el valor mínimo está en la raíz.


	Estructura Completa del Árbol:

	    Un heap es un árbol binario completo, lo que significa que todos los niveles del árbol están completamente llenos, excepto posiblemente el último nivel, que está lleno de izquierda a derecha.


	Representación:

		Un heap se puede representar de manera eficiente utilizando un array. 

		Para un nodo en la posición i del array:

			El hijo izquierdo está en la posición 2i+1.

			El hijo derecho está en la posición 2i+2. 

			El padre está en la posición [i-1/2].


	Operaciones: 	

		Inserción:

		    Agregar un nuevo elemento al final del array (último nivel del árbol) y restaurar la propiedad del heap haciendo un proceso de subida (heapify-up).

		Eliminación del Elemento Máximo o Mínimo:

		    Eliminar la raíz (el máximo en un Max-Heap o el mínimo en un Min-Heap), reemplazarla con el último elemento del array, y restaurar la propiedad del heap haciendo un proceso de bajada (heapify-down).

		Heapify:

		    Proceso para restaurar la propiedad del heap.

		    Puede ser hacia arriba (heapify-up) después de la inserción o hacia abajo (heapify-down) después de la eliminación.


	Implementación:

		```python

		class MaxHeap:
		    def __init__(self):
		        self.heap = []

		    def insert(self, element):
		        self.heap.append(element)
		        self.heapify_up(len(self.heap) - 1)

		    def delete_max(self):
		        if len(self.heap) > 1:
		            self.swap(0, len(self.heap) - 1)
		            max_value = self.heap.pop()
		            self.heapify_down(0)
		        elif self.heap:
		            max_value = self.heap.pop()
		        else:
		            max_value = None
		        return max_value

		    def heapify_up(self, index):
		        parent_index = (index - 1) // 2
		        if index > 0 and self.heap[index] > self.heap[parent_index]:
		            self.swap(index, parent_index)
		            self.heapify_up(parent_index)

		    def heapify_down(self, index):
		        largest = index
		        left_child_index = 2 * index + 1
		        right_child_index = 2 * index + 2

		        if left_child_index < len(self.heap) and self.heap[left_child_index] > self.heap[largest]:
		            largest = left_child_index

		        if right_child_index < len(self.heap) and self.heap[right_child_index] > self.heap[largest]:
		            largest = right_child_index

		        if largest != index:
		            self.swap(index, largest)
		            self.heapify_down(largest)

		    def swap(self, i, j):
		        self.heap[i], self.heap[j] = self.heap[j], self.heap[i]

		    def get_max(self):
		        if self.heap:
		            return self.heap[0]
		        return None

		# Ejemplo de uso
		heap = MaxHeap()
		elements = [3, 1, 6, 5, 2, 4]
		for element in elements:
		    heap.insert(element)

		print("Heap:", heap.heap)
		print("Max element:", heap.get_max())
		print("Deleted max element:", heap.delete_max())
		print("Heap after deletion:", heap.heap)

		```


	Aplicaciones:

		Colas de Prioridad:

		    Los heaps se utilizan para implementar colas de prioridad donde el elemento con la prioridad más alta (máxima o mínima) siempre está disponible.

		Heapsort:

		    Un algoritmo de ordenación basado en la creación de un heap y la eliminación repetida del elemento máximo o mínimo.

		Algoritmos de Grafos:

		    Utilizados en algoritmos como el de Dijkstra para encontrar el camino más corto y en el algoritmo de Prim para encontrar el árbol de expansión mínimo.



|| Grafo

	Estructura de datos fundamental en informática y matemáticas que se utiliza para representar relaciones y conexiones entre un conjunto de elementos. 

	Los grafos son extremadamente versátiles y se utilizan en una amplia variedad de aplicaciones, desde redes de computadoras hasta la representación de relaciones entre personas en redes sociales.


	Componentes:

		Vértices (Nodos):

    		Representan los objetos o entidades en un grafo.

    		Se denotan comúnmente como V o N.

		Aristas (Enlaces):

		    Representan las conexiones o relaciones entre los vértices.

		    Se denotan comúnmente como E.


	Representación:

		Lista de Adyacencia:

		    Utiliza un array o una lista donde cada posición contiene una lista de los vértices adyacentes a un vértice específico.

		    Es eficiente en términos de espacio para grafos dispersos (sparse graphs).

		Matriz de Adyacencia:

		    Utiliza una matriz n×n, donde n es el número de vértices, y el valor en la posición (i,j) indica si existe una arista entre los vértices i y j.

		    Es eficiente para grafos densos (dense graphs), pero puede consumir mucho espacio para grafos dispersos.


	Implementación:

		```python

		class Grafo:
		    def __init__(self):
		        self.grafo = {}

		    def agregar_vertice(self, vertice):
		        if vertice not in self.grafo:
		            self.grafo[vertice] = []

		    def agregar_arista(self, vertice1, vertice2):
		        if vertice1 in self.grafo and vertice2 in self.grafo:
		            self.grafo[vertice1].append(vertice2)
		            self.grafo[vertice2].append(vertice1)  # Para un grafo no dirigido

		    def mostrar_grafo(self):
		        for vertice in self.grafo:
		            print(f"{vertice}: {self.grafo[vertice]}")

		# Ejemplo de uso
		g = Grafo()
		g.agregar_vertice('A')
		g.agregar_vertice('B')
		g.agregar_vertice('C')
		g.agregar_arista('A', 'B')
		g.agregar_arista('A', 'C')
		g.agregar_arista('B', 'C')

		g.mostrar_grafo()

		```


	Aplicaciones: 

		Redes de Computadoras:

		    Modelan la conectividad y las rutas en redes de computadoras.

		Redes Sociales:

		    Representan relaciones y conexiones entre personas.

		Sistemas de Recomendación:

		    Utilizan grafos para modelar y analizar las relaciones entre usuarios y productos.

		Rutas y Navegación:

		    Utilizan grafos para encontrar rutas óptimas en sistemas de transporte y navegación.

		Análisis de Grafos:

		    Utilizados en biología para modelar redes de interacción genética y en química para modelar estructuras moleculares.



|| Algoritmos de Optimización y Programación Dinámica


    1. Algoritmos de Optimización

        Algoritmo de Dijkstra.
        Algoritmo de Bellman-Ford.


    2. Programación Dinámica

        Principios de la programación dinámica.

        Problemas clásicos (Fibonacci, Knapsack, Longest Common Subsequence).


	Algoritmos de Optimización:    

		Son métodos utilizados para encontrar la mejor solución posible (óptima) de un problema bajo un conjunto dado de restricciones. 

		Estos algoritmos tienen aplicaciones en diversas áreas, incluyendo ingeniería, economía, logística, inteligencia artificial, y ciencias de la computación. 

		Los problemas de optimización se pueden clasificar en función de varios criterios, como el 'tipo de función objetivo', la 'naturaleza de las variables' y las 'restricciones'.


		Clasificación de los Problemas de Optimización:

			1. Optimización Lineal:

			    La función objetivo y las restricciones son lineales.

			    Ejemplo: Maximizar c^Tx sujeto a Ax≤b.

			2. Optimización No Lineal:

			    La función objetivo o las restricciones son no lineales.

			    Ejemplo: Minimizar f(x) sujeto a g_i(x)≤0.

			3. Optimización Discreta:

			    Las variables de decisión son discretas (por ejemplo, enteros).

			    Ejemplo: Problemas de programación entera.

			4. Optimización Continua:

			    Las variables de decisión pueden tomar cualquier valor dentro de un rango continuo.

			    Ejemplo: Problemas de optimización sin restricciones.

			5. Optimización Combinatoria:

			    Se buscan soluciones óptimas en un espacio discreto y finito.

			    Ejemplo: Problema del Viajante (TSP).


		Algoritmos Clásicos de Optimización:

			1. Algoritmo Simplex:

    			Utilizado para problemas de optimización lineal.
    			
    			Itera sobre los vértices del conjunto factible para encontrar la solución óptima.


			2. Método de Newton:

			    Utilizado para optimización no lineal.

			    Usa derivadas de primer y segundo orden para encontrar el mínimo de una función.


			3. Descenso del Gradiente:

			    Aproximación iterativa para encontrar mínimos locales de funciones continuas y diferenciables.

			    Actualiza las variables en la dirección opuesta al gradiente de la función objetivo


			4. Programación Dinámica:

			    Descompone un problema en subproblemas más pequeños y resuelve cada uno de ellos para construir la solución óptima global.

			    Ejemplo: Problema de la mochila, Fibonacci


			5. Algoritmos Genéticos:

			    Técnicas de búsqueda heurísticas inspiradas en la evolución biológica.

			    Utilizan operadores como selección, cruce y mutación para encontrar soluciones óptimas.

			6.Algoritmo de Recocido Simulado (Simulated Annealing):

    			Inspirado en el proceso de recocido en metalurgia.

    			Permite explorar soluciones subóptimas en busca de un óptimo global.


    	Ejemplos: 

    		1. Algoritmo Simplex para Optimización Lineal:

    		```python

    		from scipy.optimize import linprog

			# Definir la función objetivo: maximizar c^T x
			c = [-1, -2]  # Coeficientes de la función objetivo

			# Definir las restricciones: Ax <= b
			A = [[2, 1], [1, 1], [1, 3]]
			b = [20, 16, 36]

			# Resolver el problema de optimización lineal
			resultado = linprog(c, A_ub=A, b_ub=b, method='simplex')

			print('Valor óptimo:', resultado.fun)
			print('Variables de decisión:', resultado.x)

    		```


    		2. Descenso del Gradiente para Optimización No Lineal:

    		```python

    		import numpy as np

			# Definir la función objetivo
			def f(x):
			    return x**2 + 4*np.sin(5*x)

			# Definir su derivada
			def df(x):
			    return 2*x + 20*np.cos(5*x)

			# Parámetros del algoritmo
			x = 2  # Valor inicial
			learning_rate = 0.01
			num_iterations = 100

			# Aplicar el algoritmo de descenso del gradiente
			for _ in range(num_iterations):
			    x -= learning_rate * df(x)

			print('Valor óptimo:', f(x))
			print('Variable de decisión:', x)

    		```


    	Aplicaciones: 

			Logística y Transporte:

			    Optimización de rutas de transporte, distribución de productos, y gestión de inventarios.

			    Ejemplo: Problema del Viajante (TSP), Problema de la mochila.

			Finanzas y Economía:

			    Optimización de carteras de inversión, análisis de riesgos, y asignación de recursos.

			    Ejemplo: Modelo de Markowitz para la optimización de carteras.

			Ingeniería y Manufactura:

			    Diseño óptimo de estructuras, optimización de procesos de fabricación, y gestión de la producción.

			    Ejemplo: Minimización de costos de producción, maximización de eficiencia.

			Inteligencia Artificial y Aprendizaje Automático:

			    Entrenamiento de modelos, ajuste de hiperparámetros, y optimización de funciones de pérdida.

			    Ejemplo: Entrenamiento de redes neuronales, métodos de ensamble.

			Ciencias de la Computación:

			    Optimización de algoritmos, asignación de tareas en sistemas distribuidos, y diseño de sistemas eficientes.

			    Ejemplo: Algoritmos de planificación, optimización de consultas en bases de datos.    		


	Programación Dinámica:

		Es una técnica de diseño de algoritmos que se utiliza para resolver problemas complejos dividiéndolos en subproblemas más simples y resolviendo cada subproblema solo una vez, almacenando sus soluciones para evitar cálculos redundantes. 

		Esta técnica es especialmente útil para problemas de optimización donde se requiere encontrar una solución óptima bajo ciertas restricciones.


		Conceptos:	

			1. Subproblemas Superpuestos:

			    La característica clave de los problemas que se pueden resolver mediante programación dinámica es que los mismos subproblemas se resuelven repetidamente. 

			    En lugar de resolverlos de nuevo cada vez que se presentan, la programación dinámica almacena sus soluciones en una tabla (a menudo llamada 'memoización').

			2. Estructura Recursiva:

			    Un problema tiene estructura recursiva si su solución óptima se puede construir eficientemente a partir de soluciones óptimas de sus subproblemas. 

			    Es decir, se puede dividir el problema original en subproblemas más pequeños de forma recursiva.

			Tabla de Memoria (Memoización):

			    Es una técnica para almacenar los resultados de los subproblemas para reutilizarlos más tarde. 

			    Esto puede implementarse utilizando matrices, diccionarios u otras estructuras de datos adecuadas.


		Estrategias de Programación Dinámica:

			Top-Down (Memoización):

			    Enfoque recursivo donde los resultados de los subproblemas se almacenan a medida que se calculan. 

			    Si un subproblema ya ha sido resuelto, su resultado se recupera de la memoria en lugar de ser recalculado.

			Bottom-Up (Tabulación):

			    Enfoque iterativo donde los subproblemas se resuelven primero y se combinan para resolver problemas más grandes. 

			    Esto generalmente implica construir una tabla de soluciones desde los subproblemas más pequeños hasta el problema original.


		Ejemplo: 

			1. Fibonacci:

    			El problema clásico de calcular el n-ésimo número de Fibonacci puede resolverse eficientemente con programación dinámica.

			```python

			def fibonacci(n):
			    # Crear una tabla para almacenar resultados de subproblemas
			    fib = [0] * (n+1)
			    # Casos base
			    fib[0] = 0
			    fib[1] = 1
			    # Llenar la tabla de manera bottom-up
			    for i in range(2, n+1):
			        fib[i] = fib[i-1] + fib[i-2]
			    return fib[n]

			print(fibonacci(10))  # Salida: 55

    		```


    		2. Problema de la Mochila (0/1 Knapsack):

    			Dado un conjunto de elementos, cada uno con un peso y un valor, determinar la combinación de elementos que maximiza el valor total sin exceder un peso máximo.

    		```python

    		def knapsack(W, weights, values, n):
			    # Crear una tabla para almacenar resultados de subproblemas
			    K = [[0 for x in range(W + 1)] for x in range(n + 1)]

			    # Llenar la tabla de manera bottom-up
			    for i in range(n + 1):
			        for w in range(W + 1):
			            if i == 0 or w == 0:
			                K[i][w] = 0
			            elif weights[i - 1] <= w:
			                K[i][w] = max(values[i - 1] + K[i - 1][w - weights[i - 1]], K[i - 1][w])
			            else:
			                K[i][w] = K[i - 1][w]
			    return K[n][W]

			values = [60, 100, 120]
			weights = [10, 20, 30]
			W = 50
			n = len(values)
			print(knapsack(W, weights, values, n))  # Salida: 220

    		```


    		3. Problema de la Secuencia Común Más Larga (Longest Common Subsequence, LCS):

    			Encontrar la longitud de la subsecuencia común más larga entre dos cadenas de caracteres.

    		```python

    		def lcs(X, Y):
			    m = len(X)
			    n = len(Y)
			    # Crear una tabla para almacenar resultados de subproblemas
			    L = [[0 for x in range(n + 1)] for x in range(m + 1)]

			    # Llenar la tabla de manera bottom-up
			    for i in range(m + 1):
			        for j in range(n + 1):
			            if i == 0 or j == 0:
			                L[i][j] = 0
			            elif X[i - 1] == Y[j - 1]:
			                L[i][j] = L[i - 1][j - 1] + 1
			            else:
			                L[i][j] = max(L[i - 1][j], L[i][j - 1])
			    return L[m][n]

			X = "AGGTAB"
			Y = "GXTXAYB"
			print(lcs(X, Y))  # Salida: 4 (GTAB)

    		```


    	Aplicaciones:

    		Optimización de Rutas:

			    Encontrar las rutas más cortas o los costos mínimos en redes, como en el algoritmo de Floyd-Warshall para rutas más cortas.

			Secuenciación de ADN:

			    Problemas de alineación de secuencias y predicción de estructuras secundarias.

			Análisis Financiero:

			    Optimización de inversiones y gestión de carteras.

			Reconocimiento de Patrones:

			    Problemas de reconocimiento de caracteres y procesamiento de imágenes.

			Planificación y Toma de Decisiones:

			    Modelos de decisión en inteligencia artificial y robótica.


		Ventajas:

    		Eficiencia: 

    			Reduce la complejidad temporal al evitar cálculos redundantes.

    		Generalidad: 

    			Puede aplicarse a una amplia variedad de problemas.


    	Desventajas: 

		    Memoria: 

		    	Puede requerir una cantidad significativa de memoria para almacenar soluciones de subproblemas.

		    Complejidad: 

		    	A veces puede ser difícil identificar la estructura recursiva y diseñar la tabla de memoización adecuada



|| Algoritmos Avanzados

	Algoritmos de Dividir y Vencerás y Greedy:

    	Dividir y Vencerás:
        	
        	Principios y ejemplos (Merge Sort, Quick Sort).


    	Algoritmos Greedy:
        	
        	Principios de algoritmos voraces.
        	
        	Problemas clásicos (Huffman Coding, Activity Selection).


    Algoritmos de Dividir y Vencerás:

    	Técnica fundamental en el diseño de algoritmos que se basa en la descomposición de un problema en subproblemas más pequeños, resolviendo cada subproblema de manera recursiva y combinando sus soluciones para obtener la solución del problema original. 

    	Esta técnica es eficaz para una amplia variedad de problemas en informática y matemáticas.


    	Conceptos: 

    		Dividir (Divide):

			    El problema se divide en varios subproblemas más pequeños que son instancias más simples del mismo problema.

			Vencer (Conquer):

			    Cada subproblema se resuelve recursivamente. 

			    Si los subproblemas son suficientemente pequeños, se resuelven directamente.

			Combinar (Combine):

			    Las soluciones de los subproblemas se combinan para formar la solución del problema original.

		
		Beneficios: 

			Eficiencia:

			    Puede reducir significativamente el tiempo de ejecución en comparación con métodos iterativos simples.

			Paralelización:

			    Los subproblemas pueden ser resueltos en paralelo, aprovechando arquitecturas de computación concurrente y distribuida.

			Claridad:

			    Facilita el diseño y la comprensión de algoritmos complejos al dividir el problema en partes manejables.


		Ejemplo: 

			1. Merge Sort:

				Un algoritmo de ordenación que divide repetidamente una lista en mitades hasta que cada sublista contiene un solo elemento, y luego combina las sublistas en una lista ordenada

			```python

			def merge_sort(arr):
			    if len(arr) > 1:
			        mid = len(arr) // 2
			        L = arr[:mid]
			        R = arr[mid:]

			        merge_sort(L)
			        merge_sort(R)

			        i = j = k = 0

			        while i < len(L) and j < len(R):
			            if L[i] < R[j]:
			                arr[k] = L[i]
			                i += 1
			            else:
			                arr[k] = R[j]
			                j += 1
			            k += 1

			        while i < len(L):
			            arr[k] = L[i]
			            i += 1
			            k += 1

			        while j < len(R):
			            arr[k] = R[j]
			            j += 1
			            k += 1

			arr = [12, 11, 13, 5, 6, 7]
			merge_sort(arr)
			print("Sorted array is:", arr)

			```


			2. Quick Sort:

    			Un algoritmo de ordenación que selecciona un 'pivote' y reordena los elementos de modo que todos los elementos menores que el pivote queden a su izquierda y los mayores a su derecha. 

    			Luego, se aplica recursivamente la misma operación a las sublistas de elementos menores y mayores.

    		```python

    		def quick_sort(arr):
			    if len(arr) <= 1:
			        return arr
			    else:
			        pivot = arr[len(arr) // 2]
			        left = [x for x in arr if x < pivot]
			        middle = [x for x in arr if x == pivot]
			        right = [x for x in arr if x > pivot]
			        return quick_sort(left) + middle + quick_sort(right)

			arr = [3, 6, 8, 10, 1, 2, 1]
			print("Sorted array is:", quick_sort(arr))

    		```


    		3. Búsqueda Binaria:

    			Un algoritmo de búsqueda eficiente en listas ordenadas que divide repetidamente el rango de búsqueda a la mitad hasta encontrar el elemento deseado o determinar que no está presente.

    		```python

    		Búsqueda Binaria:

    			Un algoritmo de búsqueda eficiente en listas ordenadas que divide repetidamente el rango de búsqueda a la mitad hasta encontrar el elemento deseado o determinar que no está presente.

    		```


    		4. Algoritmo de Strassen para la Multiplicación de Matrices:

    			Un método más rápido que el algoritmo tradicional para multiplicar matrices grandes dividiendo las matrices en submatrices más pequeñas.

    		```python

    		import numpy as np

			def strassen(A, B):
			    if A.shape[0] == 1:
			        return A * B
			    else:
			        mid = A.shape[0] // 2
			        A11 = A[:mid, :mid]
			        A12 = A[:mid, mid:]
			        A21 = A[mid:, :mid]
			        A22 = A[mid:, mid:]
			        B11 = B[:mid, :mid]
			        B12 = B[:mid, mid:]
			        B21 = B[mid:, :mid]
			        B22 = B[mid:, mid:]

			        M1 = strassen(A11 + A22, B11 + B22)
			        M2 = strassen(A21 + A22, B11)
			        M3 = strassen(A11, B12 - B22)
			        M4 = strassen(A22, B21 - B11)
			        M5 = strassen(A11 + A12, B22)
			        M6 = strassen(A21 - A11, B11 + B12)
			        M7 = strassen(A12 - A22, B21 + B22)

			        C11 = M1 + M4 - M5 + M7
			        C12 = M3 + M5
			        C21 = M2 + M4
			        C22 = M1 - M2 + M3 + M6

			        C = np.vstack((np.hstack((C11, C12)), np.hstack((C21, C22))))
			        return C

			A = np.array([[1, 2], [3, 4]])
			B = np.array([[5, 6], [7, 8]])
			print("Product of matrices:\n", strassen(A, B))

    		```


    	Ventajas: 

    	    Eficiencia: 

    	    	Puede ser más rápido que los métodos iterativos simples debido a la reducción del tamaño del problema.
		    
		    Paralelización:

		    	Subproblemas independientes pueden ser resueltos en paralelo.

		    Modularidad: 

		    	Facilita la implementación y el análisis de algoritmos complejos.


		Desventajas:

		    Sobrecarga de Recursión:

		    	El uso intensivo de recursión puede llevar a un mayor uso de la pila de llamadas, lo que puede ser ineficiente en términos de memoria.
		    
		    Complejidad de Combinación: 

		    	En algunos problemas, la etapa de combinación puede ser compleja y costosa en términos de tiempo.


    Algoritmos Greedy:

    	Técnica de diseño de algoritmos que resuelven problemas de optimización mediante la construcción de una solución paso a paso, seleccionando en cada paso la opción que parece ser la mejor en ese momento. 

    	La idea principal es tomar decisiones locales óptimas con la esperanza de encontrar una solución global óptima.


    	Características:

    		Selección de la Mejor Opción Local:

			    En cada paso, se elige la opción que parece ser la mejor en ese momento, sin considerar decisiones futuras.

			Irrevocabilidad:

			    Una vez que se toma una decisión, no se reconsidera. 

			    Las decisiones son finales y no pueden ser deshechas.

			Soluciones Constructivas:

			    La solución se construye de manera incremental, añadiendo un elemento a la vez hasta completar la solución.


		Propiedades:

			Para que un algoritmo greedy produzca una solución óptima, el problema debe cumplir con ciertas propiedades.

			Propiedad Greedy:

			    Siempre es posible tomar una decisión óptima localmente que lleva a una solución global óptima.

			Propiedad de Subestructura Óptima:

			    Una solución óptima del problema contiene soluciones óptimas de sus subproblemas.


		Ejemplos:

			1. Cambio de Monedas:

				Se da un conjunto de denominaciones de monedas y una cantidad de dinero.

				El objetivo es devolver el cambio utilizando el menor número de monedas posible.

			```python

			def cambio_monedas(monedas, cantidad):
			    resultado = []
			    for moneda in sorted(monedas, reverse=True):
			        while cantidad >= moneda:
			            cantidad -= moneda
			            resultado.append(moneda)
			    return resultado

			monedas = [1, 5, 10, 25]
			cantidad = 63
			print("Monedas usadas:", cambio_monedas(monedas, cantidad))

			```


			2. Mochila Fraccionaria:

				Se da un conjunto de objetos, cada uno con un peso y un valor. 

				El objetivo es maximizar el valor total en una mochila con capacidad limitada, permitiendo fracciones de objetos.

			```python

			class Objeto:
			    def __init__(self, peso, valor):
			        self.peso = peso
			        self.valor = valor
			        self.valor_por_peso = valor / peso

			def mochila_fraccionaria(capacidad, objetos):
			    objetos.sort(key=lambda x: x.valor_por_peso, reverse=True)
			    valor_total = 0.0
			    for objeto in objetos:
			        if capacidad > 0 and objeto.peso <= capacidad:
			            capacidad -= objeto.peso
			            valor_total += objeto.valor
			        else:
			            fraccion = capacidad / objeto.peso
			            valor_total += objeto.valor * fraccion
			            capacidad = 0
			            break
			    return valor_total

			objetos = [Objeto(10, 60), Objeto(20, 100), Objeto(30, 120)]
			capacidad = 50
			print("Valor total en la mochila:", mochila_fraccionaria(capacidad, objetos))

			```


			3. Problema del Árbol de Expansión Mínima (Algoritmo de Prim):

				Encontrar el árbol de expansión mínima en un grafo no dirigido y ponderado, conectando todos los vértices con el costo total mínimo.

			```python

			import heapq

			def prim(grafo, inicio):
			    mst = []
			    visitados = set()
			    min_heap = [(0, inicio)]
			    while min_heap:
			        costo, u = heapq.heappop(min_heap)
			        if u not in visitados:
			            visitados.add(u)
			            mst.append((costo, u))
			            for vecino, peso in grafo[u]:
			                if vecino not in visitados:
			                    heapq.heappush(min_heap, (peso, vecino))
			    return mst

			grafo = {
			    'A': [('B', 1), ('C', 4)],
			    'B': [('A', 1), ('C', 2), ('D', 5)],
			    'C': [('A', 4), ('B', 2), ('D', 1)],
			    'D': [('B', 5), ('C', 1)]
			}
			print("Árbol de expansión mínima:", prim(grafo, 'A'))

			```


		4. Problema de Huffman (Codificación de Huffman):

			Algoritmo utilizado para la compresión de datos sin pérdida que asigna códigos más cortos a los caracteres más frecuentes.

			```python

			import heapq
			from collections import defaultdict

			class Nodo:
			    def __init__(self, frecuencia, caracter=None, izquierdo=None, derecho=None):
			        self.frecuencia = frecuencia
			        self.caracter = caracter
			        self.izquierdo = izquierdo
			        self.derecho = derecho

			    def __lt__(self, otro):
			        return self.frecuencia < otro.frecuencia

			def codificacion_huffman(frecuencias):
			    heap = [Nodo(freq, char) for char, freq in frecuencias.items()]
			    heapq.heapify(heap)

			    while len(heap) > 1:
			        izquierdo = heapq.heappop(heap)
			        derecho = heapq.heappop(heap)
			        nuevo_nodo = Nodo(izquierdo.frecuencia + derecho.frecuencia, izquierdo=izquierdo, derecho=derecho)
			        heapq.heappush(heap, nuevo_nodo)

			    def construir_codigos(nodo, codigo="", codigos={}):
			        if nodo.caracter is not None:
			            codigos[nodo.caracter] = codigo
			        else:
			            construir_codigos(nodo.izquierdo, codigo + "0", codigos)
			            construir_codigos(nodo.derecho, codigo + "1", codigos)
			        return codigos

			    raiz = heap[0]
			    return construir_codigos(raiz)

			frecuencias = defaultdict(int)
			texto = "abracadabra"
			for char in texto:
			    frecuencias[char] += 1

			codigos = codificacion_huffman(frecuencias)
			print("Códigos de Huffman:", codigos)

			```



|| Clasificación de Algoritmos

	Las aplicaciones web pueden utilizar diversos tipos de algoritmos según sus objetivos y funcionalidades específicas.


	1. Algoritmos de Recomendación:

		Estos algoritmos sugieren elementos a los usuarios basándose en sus preferencias anteriores, historial de comportamiento o similitudes con otros usuarios.

		Pueden ser de filtrado colaborativo (comparando usuarios o elementos similares) o de filtrado basado en contenido (analizando las características de los elementos).


	2. Algoritmos de Búsqueda:

		Los motores de búsqueda utilizan algoritmos complejos para clasificar y presentar resultados relevantes en respuesta a las consultas de los usuarios. 

		Algoritmos como PageRank, TF-IDF (Frecuencia de Término-Inversavde Documento), y modelos de aprendizaje automático son comunes en este contexto


	3. Algoritmos de Clasificación y Categorización:

		Estos algoritmos organizan datos en categorías o etiquetas específicas. 

		Pueden incluir métodos de aprendizaje supervisado como máquinas de soporte vectorial (SVM) o clasificación de vecinos más cercanos (KNN).


	4. Algoritmos de Aprendizaje Automático (Machine Learning):

		Los algoritmos de aprendizaje automático permiten a las aplicaciones web aprender patrones y realizar tareas  específicas sin ser programados explícitamente. 

		Esto incluye algoritmos de clasificación, regresión, agrupamiento y redes neuronales, entre otros.


	5. Algoritmos de Optimización:

		Estos algoritmos buscan optimizar procesos y mejorar el rendimiento. 

		Algoritmos como el descenso del gradiente y algoritmos genéticos son ejemplos comunes utilizados para optimización en aplicaciones web.


	6. Algoritmos de Compresión:

		Para optimizar el uso de ancho de banda y mejorar los tiempos de carga, las aplicaciones web a menudo utilizan  algoritmos de compresión, como gzip o Brotli, para reducir el tamaño de los archivos antes de transmitirlos a través de la red.


	7.Algoritmos de Encriptación y Seguridad:

		En el ámbito de la seguridad, los algoritmos de encriptación (por ejemplo, AES, RSA) se utilizan para proteger la información sensible. 

		Los algoritmos de firma digital y hash también son esenciales para garantizar la integridad y autenticidad de los datos


	8. Algoritmos de Gráficos:

		Aplicaciones web que representan relaciones entre entidades a menudo utilizan algoritmos de grafos. 

		Por ejemplo, algoritmos de búsqueda en grafos como el BFS (Breadth-First Search) o DFS (Depth-First Search) son fundamentales en la navegación y análisis de redes sociales.


	9. Algoritmos de Procesamiento de Imágenes y Visión por Computadora:

		En aplicaciones web que manejan imágenes, se pueden utilizar algoritmos para realizar tareas como detección de objetos, reconocimiento facial, mejora de imágenes y segmentación de objetos.


	10. Algoritmos de Análisis de Sentimientos:

		En el contexto de redes sociales o aplicaciones que gestionan contenido generado por usuarios, los algoritmos de análisis de sentimientos pueden determinar la polaridad de un texto (positivo, negativo o neutro).


	11. Algoritmos de Routing (Enrutamiento) en Redes:
		
		Aplicaciones web que involucran navegación y geolocalización utilizan algoritmos de enrutamiento para determinar la mejor ruta entre dos ubicaciones.


|| Algoritmos de Recomendación: 

	Son sistemas inteligentes diseñados para sugerir elementos a los usuarios en función de sus preferencias, comportamientos pasados o patrones de uso. 

	Estos algoritmos se utilizan en una variedad de aplicaciones, desde plataformas de streaming y comercio electrónico hasta redes sociales y motores de búsqueda.


	1. Recopilación de Datos del Usuario:

		Los algoritmos de recomendación comienzan recopilando datos sobre el usuario. 

		Esto puede incluir información demográfica, historial de compras, patrones de navegación, interacciones anteriores y cualquier otra información relevante.


	2. Perfil de Usuario:

		Con base en los datos recopilados, se crea un perfil de usuario que refleje las preferencias y comportamientos del usuario. 

		Este perfil se utiliza como base para generar recomendaciones personalizadas.


	3. Tipos de Algoritmos de Recomendación:

		Hay varios tipos de algoritmos de recomendación, y los dos más comunes son:

		1. Filtrado Colaborativo: 

			Se basa en la idea de que si dos usuarios tienen preferencias similares en el pasado, es probable que tengan preferencias similares en el futuro. 

			Puede ser basado en el usuario (comparando usuarios similares) o basado en elementos (comparando elementos similares).


		2. Filtrado Basado en Contenido: 

			Examina las características de los elementos y sugiere nuevos elementos que comparten características similares con los elementos que le gustaron al usuario en el pasado.


	4. Matriz de Utilidad o Características:

		En el filtrado colaborativo, se crea una matriz de utilidad que contiene la información de las interacciones usuario-elemento (por ejemplo, calificaciones o clics). 

		En el filtrado basado en contenido, se construye una matriz de características para describir los elementos y sus atributos


	5. Cálculo de Similitud:

		En el filtrado colaborativo, se calcula la similitud entre usuarios o elementos en función de la matriz de utilidad. 

		En el filtrado basado en contenido, se calcula la similitud entre elementos en función de sus características.


	6. Generación de Recomendaciones:

		Una vez que se ha calculado la similitud, el algoritmo de recomendación genera recomendaciones para el usuario. 

		En el filtrado colaborativo, podría sugerir elementos que usuarios similares han encontrado útiles. 

		En el filtrado basado en contenido, podría sugerir elementos similares a los que le gustaron al usuario en el pasado.


	7. Aprendizaje Continuo:

		Los algoritmos de recomendación a menudo incorporan aprendizaje continuo. 

		Esto significa que se ajustan y mejoran con el tiempo a medida que el usuario interactúa con las recomendaciones y se recopila más información sobre sus preferencias.


	8. Evaluación y Retroalimentación:

		Se evalúan las recomendaciones en función de la retroalimentación del usuario.

		Si el usuario interactúa positivamente con las recomendaciones, el sistema aprende y ajusta su modelo. 
		
		La retroalimentación negativa también se utiliza para refinar y mejorar las recomendaciones futuras



|| Algoritmos de Busqueda: 

	Se refiere a un conjunto de pasos o reglas bien definidas que se utilizan para encontrar una solución a un problema específico. 

	Estos algoritmos se aplican comúnmente en contextos donde se necesita ubicar un elemento particular dentro de un conjunto de datos, ya sea para recuperar información, verificar la existencia de un elemento o encontrar la posición de un elemento en una lista.


	1. Búsqueda Secuencial:

		La búsqueda secuencial es el método más simple y directo.

		Consiste en recorrer los elementos uno por uno hasta encontrar el que se busca o llegar al final del conjunto de datos. 

		Es eficaz para conjuntos de datos pequeños, pero puede volverse ineficiente para conjuntos más grandes.


	2. Búsqueda Binaria:

		La búsqueda binaria es un algoritmo eficiente aplicado a conjuntos de datos ordenados. 

		Se basa en la idea de dividir repetidamente el conjunto a la mitad y descartar la mitad no deseada hasta encontrar el elemento deseado.

		Este algoritmo funciona mejor en conjuntos de datos ordenados y tiene una complejidad temporal logarítmica.


	3. Búsqueda en Profundidad (DFS):

		La búsqueda en profundidad es un algoritmo utilizado en grafos para explorar lo más posible a lo largo de cada rama antes de retroceder. 

		Es comúnmente utilizado para resolver problemas de grafos, como encontrar rutas en un laberinto o realizar recorridos


	4. Búsqueda en Amplitud (BFS):

		A diferencia de la búsqueda en profundidad, la búsqueda en amplitud explora todos los vecinos de un nodo antes de pasar al siguiente nivel.

		Es útil para encontrar la ruta más corta entre dos nodos en un grafo no ponderado.


	5. Algoritmo A:*

		El algoritmo A* es un algoritmo de búsqueda heurística que combina la búsqueda en amplitud con una función heurística que estima el costo desde un nodo hasta el objetivo. 

		Es comúnmente utilizado en problemas de búsqueda de rutas en grafos.


	6. Búsqueda Exponencial:

		La búsqueda exponencial es un método que aprovecha la estructura de un espacio de búsqueda para reducir la cantidad de nodos que deben ser evaluados. 

		Puede ser útil en problemas donde hay un conjunto de soluciones que pueden ser descartadas eficientemente


	7. Búsqueda de Patrones (Substring Search):

		Estos algoritmos buscan la ocurrencia de un patrón (subcadena) dentro de una cadena más grande. 

		Ejemplos incluyen el algoritmo de fuerza bruta, el algoritmo de Knuth-Morris-Pratt (KMP) y el algoritmo Boyer-Moore.


	8. Búsqueda de Hashing:

		Utiliza funciones hash para buscar eficientemente elementos en un conjunto de datos. 

		Los algoritmos de búsqueda basados en hashing, como las tablas hash, son rápidos para búsquedas exactas-


	9. Búsqueda Local:

		Este tipo de algoritmo comienza con una solución inicial y mejora iterativamente la solución cambiando gradualmente hacia soluciones vecinas hasta encontrar una solución óptima o satisfactoria.


	La elección del algoritmo dependerá de la naturaleza del 
	problema y la estructura de los datos. 

	La eficiencia y la complejidad de cada algoritmo pueden
	variar según el contexto en el que se aplican.



|| Algoritmo de Clasificación y Categorización: 

	Son técnicas utilizadas en aprendizaje automático e inteligencia artificial para organizar datos en categorías o clases específicas. 

	El objetivo principal es asignar etiquetas o categorías a datos no etiquetados en función de patrones y características identificadas durante el entrenamiento del algoritmo.


	1. Aprendizaje Supervisado:

		Los algoritmos de clasificación y categorización a menudo se basan en el aprendizaje supervisado. 

		En este enfoque, el algoritmo se entrena utilizando un conjunto de datos que ya está etiquetado con las categorías correctas.


	2. Características y Atributos:

		Los datos en el conjunto de entrenamiento se describen mediante características o atributos relevantes. 

		Estos atributos son las propiedades que el algoritmo utilizará para realizar la clasificación.


	3. Modelo de Clasificación:

		Durante la fase de entrenamiento, el algoritmo utiliza el conjunto de datos etiquetado para construir un modelo de clasificación. 

		Este modelo captura patrones y relaciones entre las características y las etiquetas asociadas.


	4. Clases o Categorías:

		Las clases o categorías son las etiquetas que el algoritmo intentará asignar a datos no etiquetados durante la fase de predicción. 

		Por ejemplo, en un problema de clasificación de imágenes, las clases podrían ser "perro", "gato", "automóvil", etc


	5. Algoritmos de Clasificación Comunes:

		Hay varios algoritmos de clasificación comúnmente utilizado:
	       
		Regresión Logística: 

			Utilizada para problemas de clasificación binaria.

        
		Máquinas de Soporte Vectorial (SVM): 

			Puede aplicarse a problemas de clasificación binaria y multiclase.


		Árboles de Decisión: 

			Estructuras de decisión que se ramifican en función de las características.


		K-Vecinos Más Cercanos (KNN): 

			Asigna la categoría basándose en la mayoría de las clases cercanas.


		Redes Neuronales:

			Modelos inspirados en el funcionamiento del cerebro que pueden manejar problemas complejos de clasificación.


	6. Validación del Modelo:

		Después de entrenar el modelo, se debe evaluar su rendimiento utilizando datos no utilizados durante el entrenamiento. 

		Técnicas como la validación cruzada pueden ayudar a garantizar que el modelo sea capaz de generalizar bien a datos nuevos


	7. Clasificación Multiclase y Multietiqueta:

		Algunos problemas de clasificación implican más de dos clases (multiclase), mientras que otros pueden asignar múltiples etiquetas a una instancia (multietiqueta)


	8.Aplicaciones Prácticas:

		Los algoritmos de clasificación se utilizan en diversas aplicaciones, como reconocimiento de imágenes, procesamiento de lenguaje natural, diagnóstico médico, sistemas de recomendación y filtrado de spam, entre otros. 


	9. Problemas de Desbalance de Clases:

		En casos donde hay un desbalance significativo entre el número de instancias en diferentes clases, es importante abordar este desafío para evitar sesgos en la clasificación.


	10. Ajuste de Hiperparámetros:

		Muchos algoritmos de clasificación tienen hiperparámetros que afectan su rendimiento. 

		Ajustar estos parámetros es crucial para optimizar el modelo.


	Los algoritmos de clasificación y categorización son esenciales en el ámbito del aprendizaje automático y juegan un papel fundamental en la automatización de la toma de decisiones basada en datos.



|| Metodos de Aprendisaje Supervisado: 

	Son técnicas en el campo del aprendizaje automático donde un algoritmo se entrena utilizando un conjunto de datos etiquetado. 

	En este enfoque, el conjunto de datos de entrenamiento contiene ejemplos de entrada junto con sus salidas correspondientes, lo que permite al algoritmo aprender la relación entre las entradas y las salidas. 

	El objetivo final es que el modelo pueda hacer predicciones precisas sobre nuevas instancias no vistas.


	1. Regresión Lineal:

		La regresión lineal es utilizada para problemas de predicción numérica. 

		Busca encontrar la mejor línea (o hiperplano en dimensiones superiores) que se ajuste a los datos de entrenamiento.


	2. Regresión Logística:

		Aunque su nombre incluye "regresión", la regresión logística se utiliza para problemas de clasificación binaria. 

		Estima la probabilidad de pertenencia a una clase y aplica una función logística  para convertir esa probabilidad en una clasificación.


	3. Máquinas de Soporte Vectorial (SVM):

		Las SVM son algoritmos versátiles utilizados tanto para problemas de clasificación como de regresión. 

		Buscan encontrar un hiperplano que maximice el margen entre clases.


	4. Árboles de Decisión:

		Los árboles de decisión dividen repetidamente el conjunto de datos en subconjuntos más pequeños en función de las características, formando una estructura de árbol. 

		Se utilizan para clasificación y regresión.


	5. K-Vecinos Más Cercanos (KNN):

		KNN clasifica una instancia según las clases de sus vecinos más cercanos en el espacio de características. 

		Es simple pero puede ser poderoso para datos no lineales.


	6. Redes Neuronales Artificiales:

		Las redes neuronales son modelos computacionales inspirados en el funcionamiento del cerebro. 

		Se utilizan para una amplia variedad de problemas, desde reconocimiento de patrones hasta procesamiento de lenguaje natural.


	7. Naive Bayes:

		Basado en el teorema de Bayes, el clasificador Naive Bayes asume que las características son independientes entre sí, lo que facilita los cálculos y permite una clasificación rápida.


	8. Bosques Aleatorios (Random Forest):

		Los bosques aleatorios son conjuntos de árboles de decisión que se entrenan de manera independiente y luego combinan sus predicciones. 

		Proporcionan un modelo más robusto y menos propenso al sobreajuste.


	9. Gradient Boosting:

		El aumento de gradiente construye un modelo en etapas, cada vez mejorando las deficiencias del modelo anterior.

		Es eficaz para problemas de regresión y clasificación


	10. Máquinas de Aprendizaje Extremo (Extreme Learning Machines - ELM):

		Las ELM son redes neuronales de una sola capa oculta donde los pesos entre las capas oculta y de salida se establecen aleatoriamente y se ajustan mediante una simple operación de inversión matricial


	11. Máquinas de Vectores de Soporte (Support Vector Machines - SVM) para Regresión:

		Al igual que en la clasificación, las SVM también se pueden aplicar a problemas de regresión, donde buscan ajustar una línea o superficie que minimice el error.


	12. Máquinas de Vectores de Soporte (Support Vector Machines - SVM) para Clasificación Multiclase:

		Las SVM también se pueden extender para manejar problemas de clasificación con más de dos clases mediante la técnica "uno contra todos" o "uno contra uno".


	Son solo algunos ejemplos de métodos de aprendizaje supervisado. 

	La elección del método depende de la naturaleza del problema y del tipo de datos disponibles. 

	Cada método tiene sus ventajas y desventajas, y su rendimiento puede variar según el contexto de aplicación.



|| Algoritmos de Optimización: 

	Son técnicas utilizadas para encontrar la mejor solución posible o el conjunto óptimo de soluciones en un problema específico, generalmente caracterizado por una función objetivo que se debe maximizar o minimizar. 

	Estos algoritmos desempeñan un papel crucial en diversas áreas, como la ingeniería, la ciencia de datos, la inteligencia artificial y la investigación operativa.


	1. Función Objetivo:

		La función objetivo es una medida cuantitativa que se desea maximizar o minimizar. 

		Puede representar la eficiencia, el rendimiento, el costo, la utilidad u otro criterio relevante según el contexto del problema.


	2. Variables de Decisión:

		Las variables de decisión son las variables que pueden ajustarse o configurarse para encontrar la solución óptima.

		Estas variables afectan directamente el valor de la función objetivo.


	3. Condiciones y Restricciones:

		Los problemas de optimización a menudo incluyen condiciones o restricciones que las soluciones deben cumplir. 

		Estas restricciones pueden ser lineales o no lineales y afectan las posibles soluciones del problema.


	4. Optimización Continua y Discreta:

		La optimización continua se refiere a problemas donde las variables de decisión pueden tomar cualquier valor en un rango continuo, mientras que la optimización discreta implica variables que deben ser enteras o pertenecer a un conjunto discreto.


	5. Algoritmos de Descenso de Gradiente:

		Los algoritmos de descenso de gradiente son comunes en la optimización de funciones continuas. 

		Buscan iterativamente ajustar las variables de decisión en la dirección opuesta al gradiente  de la función objetivo


	6. Algoritmos Evolutivos:

		Inspirados en la evolución biológica, los algoritmos evolutivos generan una población de soluciones, aplican operadores de selección, cruza y mutación, y evalúan la aptitud de cada solución para evolucionar hacia soluciones óptimas.


	7. Métodos de Programación Lineal y No Lineal:

		La programación lineal y no lineal aborda problemas con restricciones lineales o no lineales.

		El método de programación lineal busca maximizar o minimizar una función lineal sujeta a restricciones lineales.


	8. Algoritmos de Optimización Heurística:

		Estos algoritmos no garantizan encontrar la solución óptima, pero son eficientes para problemas complejos. 

		Ejemplos incluyen la búsqueda tabú, el recocido simulado y los algoritmos genéticos.


	9. Métodos de Cuadrados Mínimos:

		Utilizados en regresión y ajuste de curvas, los métodos de cuadrados mínimos buscan minimizar la suma de los cuadrados de las diferencias entre los valores observados y los predichos.


	10. Optimización Multiobjetivo:

		En problemas con múltiples objetivos, la optimización multiobjetivo busca encontrar soluciones que optimicen varios criterios simultáneamente, lo que da como resultado un conjunto de soluciones pareto-óptimas.


	11. Algoritmos de Optimización Cuántica:

		Inspirados en la computación cuántica, estos algoritmos utilizan principios cuánticos para buscar soluciones eficientes para problemas de optimización.


	12. Optimización Estocástica:

		En problemas con incertidumbre o variabilidad, la optimización estocástica incorpora elementos probabilísticos en el proceso de toma de decisiones.

		La elección del algoritmo depende de la naturaleza específica del problema y los requisitos del contexto en el que se aplica.



|| Algoritmos de Regresión: 

	Son técnicas en estadísticas y aprendizaje automático utilizadas para modelar la relación entre una variable dependiente (o de respuesta) y una o más variables independientes (o características).

	El objetivo principal de la regresión es prever o estimar el valor de la variable dependiente basándose en las variables independientes.


	1. Regresión Lineal Simple:

		En la regresión lineal simple, se asume una relación lineal entre la variable dependiente y una única variable independiente.

		La línea de mejor ajuste se encuentra minimizando la suma de los cuadrados de las diferencias entre los valores observados y los predichos.


	2. Regresión Lineal Múltiple:

		La regresión lineal múltiple extiende el concepto de regresión lineal simple para incluir múltiples variables independientes.

		El modelo busca una relación lineal que explique la variabilidad en la variable dependiente


	3. Regresión Polinómica:

		La regresión polinómica permite modelar relaciones no lineales entre variables ajustando un polinomio a los datos. 

		Puede capturar curvas y patrones más complejos


	4. Regresión de Vecino Más Cercano (KNN):

		KNN se puede utilizar para problemas de regresión. 

		Para prever el valor de la variable dependiente, se promedian los valores de las k instancias más cercanas en el espacio de características.


	5. Regresión Ridge y Regresión LASSO:

		Estos métodos introducen regularización para evitar el sobreajuste. 

		Ridge (L2) y LASSO (L1) penalizan ciertos términos en la función de pérdida para controlar la complejidad del modelo.


	6. Regresión de Bosques Aleatorios (Random Forest):

		Los bosques aleatorios pueden utilizarse para regresión al promediar las predicciones de múltiples árboles de decisión.

		Proporcionan un modelo robusto y menos propenso al sobreajuste.


	7. Máquinas de Soporte Vectorial (SVM) para Regresión:

		Las SVM también se pueden aplicar a problemas de regresión.

		Buscan encontrar un hiperplano que maximice el margen entre las instancias de entrenamiento.


	8. Regresión Bayesiana:

		La regresión bayesiana incorpora el teorema de Bayes para modelar la incertidumbre y actualizar las creencias sobre los parámetros del modelo a medida que se observan nuevos datos.


	9. Redes Neuronales para Regresión:

		Las redes neuronales pueden utilizarse para problemas de regresión al ajustar los pesos y sesgos de las conexiones entre las capas para minimizar la diferencia entre las predicciones y los valores reales.


	10. Regresión Quantílica:

		La regresión quantílica se utiliza para modelar diferentes cuantiles de la distribución condicional de la variable dependiente, proporcionando información detallada sobre diferentes partes de la distribución.


	11. Regresión Logística:

		Aunque a menudo se asocia con la clasificación binaria, la regresión logística se puede utilizar en problemas de regresión cuando la variable dependiente es binaria.


	12. Aprendizaje Automático Explicativo (LIME):

		Aunque no es un algoritmo de regresión en sí mismo, LIME es una técnica que se utiliza para explicar modelos de aprendizaje automático, incluidos los modelos de regresión, descomponiéndolos en términos interpretables.


	La elección del algoritmo de regresión depende de la naturaleza del problema, la relación esperada entre las variables y otros factores como la cantidad de datos disponibles y la interpretabilidad del modelo.



|| Algoritmos de Agrupamiento: 

	Son técnicas utilizadas en estadísticas y aprendizaje automático para dividir un conjunto de datos en grupos o clústeres con base en la similitud entre las instancias. 

	A diferencia de los algoritmos de clasificación, en los cuales se conoce de antemano la pertenencia a una clase específica, los algoritmos de agrupamiento buscan identificar patrones intrínsecos en los datos sin etiquetas previas.


	1. K-Means:

		K-Means es uno de los algoritmos de agrupamiento más populares. 

		Divide el conjunto de datos en k clústeres, donde k es un parámetro predefinido. 

		Busca minimizar la varianza dentro de cada clúster.

 
	2. Agrupamiento Jerárquico:

		Los algoritmos jerárquicos crean una estructura de árbol que representa la jerarquía de clústeres. 

		Pueden ser aglomerativos (comenzando con instancias individuales y fusionándolas) o divisivos (comenzando con un clúster único y dividiéndolo).


	3. DBSCAN (Density-Based Spatial Clustering of 
	Applications with Noise):

		DBSCAN agrupa instancias en áreas densas del espacio de características, definiendo clústeres como regiones con densidad suficientemente alta separadas por regiones con baja densidad.


	4. Mean Shift:

		Mean Shift es un algoritmo de agrupamiento basado en la búsqueda de modas en la distribución de datos. 

		Encuentra los picos o modas en la densidad de datos y asigna instancias a los clústeres correspondientes.


	5. Algoritmo de Expectation-Maximization (EM):

		EM es un algoritmo de agrupamiento que también se utiliza en problemas de estimación de parámetros. 

		En el contexto de agrupamiento, se utiliza para modelar distribuciones mixtas y asignar instancias a clústeres.


	6. Spectral Clustering:

		Spectral Clustering utiliza la estructura espectral del grafo de similitud entre instancias para realizar el agrupamiento. 

		Es eficaz para detectar estructuras no lineales.


	7. OPTICS (Ordering Points To Identify the Clustering Structure):

		OPTICS es un algoritmo de agrupamiento basado en la densidad que genera una representación ordenada de los datos, lo que permite identificar clústeres de diferentes densidades y formas.


	8. Affinity Propagation:

		Affinity Propagation utiliza la propagación de afinidad entre instancias para encontrar automáticamente el número de clústeres. 

		Cada instancia actúa como un representante del clúster y se envían mensajes de afinidad entre ellas.


	9. Fuzzy C-Means:

		Fuzzy C-Means es una extensión del algoritmo K-Means que asigna grados de pertenencia de las instancias a múltiples clústeres en lugar de asignarlas de manera rígida a un solo clúster.


	10. Self-Organizing Maps (SOM):

		SOM es un tipo de red neuronal no supervisada que proyecta instancias de datos en un espacio bidimensional o tridimensional, preservando la topología de las relaciones entre ellas.


	11. Algoritmos de Agrupamiento Basados en Grafos:

		Algoritmos como el algoritmo de corte espectral y el algoritmo de Louvain utilizan técnicas de teoría de grafos para realizar el agrupamiento.


	12. Clustering basado en Particionamiento Espectral 
	(Spectral Partitioning):

		Utiliza técnicas de álgebra lineal y la estructura espectral de la matriz de similitud para particionar el conjunto de datos en clústeres.


	La elección del algoritmo de agrupamiento depende de la naturaleza de los datos y del tipo de clústeres que se esperan. 

	Algunos algoritmos son más adecuados para clústeres de
	formas y tamaños irregulares, mientras que otros son eficaces para datos de alta densidad o con estructuras no lineales.



|| Redes Neuronales
	
	Son modelos computacionales inspirados en la estructura y el funcionamiento del cerebro humano. 

	Estos modelos se utilizan en el campo del aprendizaje automático y la inteligencia artificial para abordar problemas de clasificación, regresión, reconocimiento de patrones y otras tareas. 

	La estructura de una red neuronal se compone de unidades llamadas neuronas, organizadas en capas y conectadas mediante conexiones ponderadas.


	1. Neurona Artificial:

		Una neurona artificial es la unidad básica de una red neuronal. 

		Recibe múltiples entradas, aplica una función de activación a la combinación ponderada de esas entradas y produce una salida.


	2. Capas de una Red Neuronal:

		Las redes neuronales típicamente constan de capas:
	        
		1. Capa de Entrada: 
			
			Recibe las características o atributos de entrada.

		2. Capas Ocultas: 
			
			Realizan transformaciones no lineales de los datos.

		3. Capa de Salida: 
			
			Produce la salida final del modelo.


	3. Conexiones Ponderadas:

		Cada conexión entre neuronas tiene un peso asociado que determina la importancia de la entrada en la salida. 

		Durante el entrenamiento, estos pesos se ajustan para mejorar el rendimiento del modelo.


	4. Funciones de Activación:

		Las funciones de activación se aplican a la combinación ponderada de las entradas en cada neurona para introducir no linealidades en el modelo. 

		Ejemplos incluyen la función sigmoide, la función de tangente hiperbólica (tanh) y la función de rectificación lineal (ReLU).


	5. Aprendizaje Supervisado:

		En el aprendizaje supervisado, las redes neuronales se entrenan utilizando un conjunto de datos etiquetado, donde la red ajusta sus pesos para minimizar la diferencia entre las predicciones y las etiquetas reales.


	6. Retropropagación (Backpropagation):

		Es el algoritmo utilizado para entrenar redes neuronales. 

		Consiste en propagar el error desde la capa de salida hacia atrás, ajustando los pesos en función de la magnitud del error.


	7. Función de Pérdida:

		La función de pérdida mide la discrepancia entre las predicciones del modelo y las etiquetas reales. 

		Durante el entrenamiento, se busca minimizar esta función.


	8. Redes Neuronales Convolucionales (CNN):

		Diseñadas para procesar datos de tipo gráfico, como imágenes. 

		Utilizan capas convolucionales para aprender patrones espaciales y jerarquías de características.


	9. Redes Neuronales Recurrentes (RNN):

		Diseñadas para manejar datos secuenciales, como series temporales o texto. 

		Contienen conexiones que retroalimentan la información a capas anteriores, permitiendo la retención de información a lo largo del tiempo.


	10. Redes Neuronales Profundas (Deep Learning):

		Se refiere a modelos de redes neuronales con múltiples capas ocultas. 

		La profundidad de la red permite aprender representaciones más complejas y abstractas de los datos.


	11. Autoencoders:

		Tipo de red neuronal utilizada para aprendizaje no supervisado y reducción de dimensionalidad. 

		Consiste en una capa de codificación y una capa de decodificación.


	12. Transfer Learning:

		Estrategia que consiste en utilizar una red neuronal  preentrenada en una tarea específica y adaptarla a una tarea relacionada. 

		Esto acelera el entrenamiento y puede mejorar el rendimiento.


	Las redes neuronales han demostrado ser muy efectivas en una amplia gama de aplicaciones, desde reconocimiento de imágenes y procesamiento de lenguaje natural hasta juegos y conducción autónoma. 

	La arquitectura y la configuración de una red neuronal pueden variar según la tarea específica que se esté abordando.



|| Algoritmos de Redes Neuronales: 

	Existen varios algoritmos y arquitecturas asociadas con redes neuronales en el campo del aprendizaje automático y la inteligencia artificial.


	1. Perceptrón:

		El perceptrón es la unidad más básica de una red neuronal.

		Se utiliza para realizar una clasificación binaria y puede aprender a través del algoritmo de aprendizaje supervisado basado en la regla de perceptrón.


	2. Algoritmo de Retropropagación (Backpropagation):

		Backpropagation es un algoritmo de entrenamiento fundamental para redes neuronales con múltiples capas. 

		Se utiliza en el aprendizaje supervisado y ajusta los pesos de las conexiones entre neuronas para minimizar la diferencia entre las predicciones y las etiquetas reales.


	3. Redes Neuronales Multicapa (MLP):

		Las redes neuronales multicapa son una extensión del perceptrón y consisten en capas de neuronas organizadas en una estructura multicapa. 

		La retropropagación se utiliza para entrenar MLP.


	4. Funciones de Activación:

		Las funciones de activación, como la sigmoide, la tangente hiperbólica (tanh) y la rectificación lineal (ReLU), son esenciales para introducir no linealidades en las redes neuronales y permitir la representación de relaciones complejas.


	5. Redes Neuronales Convolucionales (CNN):

		Diseñadas específicamente para tareas relacionadas con datos espaciales, como imágenes. 

		Utilizan capas convolucionales para aprender patrones locales y jerarquías de características.


	6. Redes Neuronales Recurrentes (RNN):

		Apropiadas para datos secuenciales, como series temporales o texto.

		Las RNN tienen conexiones retroalimentadas que permiten la retención de información a lo largo del tiempo.


	7. LSTM (Long Short-Term Memory):

		Una variante de las RNN que aborda el problema del olvido del gradiente. 

		Las LSTM incorporan unidades de memoria que pueden mantener y actualizar información a lo largo del tiempo.


	8. GRU (Gated Recurrent Unit):
		
		Similar a las LSTM, las GRU también son una variante de las RNN. 

		Tienen una estructura simplificada con puertas de actualización y reinicio.


	9. Autoencoders:

		Los autoencoders son redes neuronales utilizadas en aprendizaje no supervisado y reducción de dimensionalidad. 

		Consisten en una capa de codificación y una capa de decodificación.


	10. Redes Neuronales Generativas Adversarias (GAN):

		GANs son un tipo especial de red neuronal que consta de un generador y un discriminador. 

		El generador crea muestras que intentan pasar como reales, mientras que el discriminador intenta distinguir entre las muestras reales y generadas.


	11. Redes Neuronales Siamesas:

		Las redes neuronales siamesas se utilizan para aprender representaciones similares entre pares de entradas. 

		Se utilizan en tareas de comparación y clasificación de similitud.


	12. Redes Neuronales Preentrenadas:

		La transferencia de aprendizaje es una estrategia que implica utilizar una red neuronal preentrenada en una tarea específica y ajustarla para una tarea relacionada. 

		Esto se hace comúnmente con arquitecturas como VGG, ResNet y BERT.


	13. Redes Neuronales Bayesianas:

		Incorporan conceptos de probabilidad y bayesianismo en la modelización de incertidumbre. 

		Estas redes pueden ser útiles en tareas donde se necesita tener en cuenta la variabilidad y la incertidumbre en las predicciones.


	14. Redes Neuronales Recurrentes Atencionales (Attention):

		Mejoran la capacidad de las RNN para manejar secuencias largas al permitir que el modelo se enfoque selectivamente en partes específicas de la entrada.



|| Algoritmo de Aprendizaje Continuo
	
	Se refiere a algoritmos de aprendizaje automático (machine learning) que tienen la capacidad de adaptarse y mejorar continuamente a medida que se les proporciona más información o datos. 

	Estos algoritmos están diseñados para ajustar sus modelos y predicciones a medida que se acumulan nuevos datos, permitiendo una actualización constante del conocimiento del sistema.


	1. Aprendizaje Incremental:

		Los algoritmos de aprendizaje continuo operan de manera incremental, es decir, pueden aprender y ajustarse a nuevos datos sin tener que volver a entrenar desde cero con el conjunto de datos completo.


	2. Adaptabilidad:

		Estos algoritmos son adaptables a cambios en el entorno o en los patrones de datos. 
		
		Pueden modificar sus modelos internos para reflejar mejor la naturaleza actual de los datos.


	3. Actualización Automática:

		A medida que se introducen nuevos datos, el algoritmo de aprendizaje continuo actualiza automáticamente sus parámetros o estructuras de modelo para mejorar su capacidad predictiva.


	4. Uso de Streams de Datos:

		A menudo, los algoritmos de aprendizaje continuo se utilizan en entornos donde los datos llegan en forma de secuencias o "streams", en lugar de lotes estáticos. 

		Esto es común en aplicaciones que manejan datos en tiempo real.


	5. Mejora de la Generalización:

		La capacidad de aprendizaje continuo puede contribuir a una mejor generalización del modelo, ya que se adapta a la evolución de los patrones en lugar de depender exclusivamente de los datos históricos.


	6. Desafíos en la Estabilidad del Modelo:

		Un desafío común en el aprendizaje continuo es mantener la estabilidad del modelo a medida que se actualiza. 

		Demasiada adaptación a datos ruidosos o no representativos puede llevar a un sobreajuste o a cambios en la calidad de las predicciones.


	7. Aprendizaje Online:

		El aprendizaje continuo a menudo se asocia con el concepto de "aprendizaje online", donde el modelo se actualiza de manera incremental a medida que llegan nuevos datos, sin necesidad de volver a entrenar con el conjunto de datos completo.


	8. Aplicaciones Prácticas:

		Los algoritmos de aprendizaje continuo son útiles en casos en los que los datos evolucionan con el tiempo, como en el análisis de comportamientos del usuario en aplicaciones web, sistemas de recomendación en tiempo real y en la detección de cambios en patrones de tráfico.



|| Algoritmo de Retropropagación: 

	También conocido como retropropagación del error, es un  algoritmo de aprendizaje supervisado utilizado en redes neuronales artificiales. 

	Su objetivo es ajustar los pesos de una red neuronal para minimizar la diferencia entre las salidas predichas y las salidas deseadas para un conjunto de datos de entrenamiento.

	Este algoritmo es fundamental en el entrenamiento de redes neuronales para tareas como clasificación o regresión.



|| Algoritmo de Compresión: 

	Son técnicas utilizadas para reducir el tamaño de archivos o datos, lo que permite ahorrar espacio de almacenamiento y facilita la transmisión rápida de información. 

	Hay dos tipos principales de compresión: 

		la compresión sin pérdida y la compresión con pérdida.


	1. Compresión Sin Pérdida

		Codificación de Longitud de Carrera (Run-Length Encoding - RLE):

			Sustituye secuencias repetitivas de datos con un solo valor y el número de repeticiones. 

			Es eficiente para datos con patrones repetitivos.


		Códigos de Huffman:

			Asigna códigos de longitud variable a los símbolos según su frecuencia de aparición en los datos. 

			Símbolos más comunes tienen códigos más cortos.


		Códigos de Longitud de Prefijo (Prefix Codes):

			Similar a los códigos de Huffman, asigna códigos a los símbolos de manera que ningún código sea prefijo de otro, lo que facilita la decodificación.


		Compresión LZ77 y LZ78:

			Utiliza diccionarios para reemplazar secuencias repetitivas de datos con referencias a una copia previamente vista de esos datos.


		Algoritmo Burrows-Wheeler (BWT):

			Reorganiza los caracteres en una cadena para que las secuencias similares estén juntas. 

			Luego se utiliza la transformada de Huffman para la compresión adicional



	2. Compresión Con Pérdida:

		Transformada Discreta del Coseno (Discrete Cosine Transform - DCT):

			Utilizado en JPEG, transforma bloques de píxeles en una representación en el dominio de la frecuencia, donde se pueden cuantificar y codificar con pérdida.


		Transformada de Onda (Wavelet Transform):

			Utilizado en formatos como JPEG2000, divide la imagen en bandas de frecuencia, permitiendo la compresión selectiva
			de ciertas componentes.


		Compresión con Pérdida de Audio (MP3):

			Utiliza algoritmos como la Transformada de Fourier y la Compresión de Huffman para reducir el tamaño de archivos de audio eliminando cierta información percibida como menos relevante.


		Compresión de Video (H.264, HEVC):

			Utiliza técnicas de compresión de imagen y audio junto con métodos específicos para video, como la compensación de 
			movimiento, para reducir el tamaño de archivos de video.


		Compresión de Texto con Pérdida (LZ77 con Cuantificación Vectorial):

			Combina la compresión de texto sin pérdida con técnicas de cuantificación vectorial para comprimir texto con 
			pérdida.



	3. Consideraciones y Desafíos:

		Tasa de Compresión:

			La medida de cuánto se reduce el tamaño del archivo en comparación con el original.


		Velocidad de Compresión y Descompresión:

			La eficiencia en términos de tiempo que toma realizar la compresión y descompresión.


		Calidad de la Recuperación:

			En compresión con pérdida, cuánta información original se puede recuperar y qué tan perceptible es la pérdida.


		Usos Específicos:

			Algunos algoritmos son más adecuados para ciertos tipos de datos (imágenes, audio, texto) o aplicaciones específicas.


		Uso de Recursos:

			Algoritmos más avanzados pueden requerir más recursos computacionales para la compresión y descompresión.


	La elección del algoritmo de compresión depende de la naturaleza de los datos, los requisitos de calidad y rendimiento, y la aplicación específica. 

	La compresión es esencial en muchos aspectos de la informática moderna, desde la transmisión eficiente de datos hasta el almacenamiento optimizado.



|| Algoritmo de Encriptación y Seguridad:

	La encriptación y la seguridad informática son aspectos fundamentales para proteger la confidencialidad y la integridad de la información. 

	Un algoritmo de encriptación es una serie de pasos matemáticos utilizados para transformar datos en un formato ilegible, conocido como cifrado, con el objetivo de que solo aquellos que posean la clave adecuada puedan revertir este proceso y acceder a la información original


	Algoritmos de Encriptación:

		1. Simétricos (o de clave privada):

			Utilizan la misma clave para encriptar y desencriptar la información. 

			Ejemplos incluyen DES (Data Encryption Standard), AES (Advanced Encryption Standard) y 3DES.


		2. Asimétricos (o de clave pública):

			Utilizan pares de claves, una pública y otra privada. 

			La clave pública se comparte libremente, mientras que la clave privada se mantiene en secreto. 

			Ejemplos incluyen RSA (Rivest-Shamir-Adleman) y ECC (Elliptic Curve Cryptography).


		3. Hashing:

			Aunque no es técnicamente encriptación, los algoritmos de hashing transforman datos en una cadena de caracteres fija, generalmente un valor hash. 

			Este valor es único para un conjunto de datos dado y no se puede revertir. 

			SHA-256 (Secure Hash Algorithm 256-bit) es un ejemplo.


	Conceptos de Seguridad Informática:

		1. Integridad de Datos:

			Garantizar que la información no ha sido alterada accidental o intencionalmente durante la transmisión o el almacenamiento.


		2. Confidencialidad:

			Proteger la información contra accesos no autorizados. 

			La encriptación es una herramienta fundamental para lograr la confidencialidad.


		3. Autenticación:

			Verificar la identidad de una entidad, ya sea un usuario o un sistema. 

			Métodos como contraseñas, certificados digitales y biometría son comunes.


		4. Autorización:

			Determinar qué acciones o recursos están permitidos para un usuario autenticado.


		5. Firma Digital:

			Utilizada para garantizar la autenticidad e integridad de un mensaje o documento digital. 

			Se basa en el uso de claves públicas y privadas.


		6. Gestión de Claves:

			Asegurar la generación, distribución y almacenamiento seguros de claves criptográficas.


		7. Ataques y Contramedidas:

			Comprender y defenderse contra ataques comunes como fuerza bruta, ataques de diccionario, ataques de intermediarios (man-in-the-middle), etc.


		8. Criptoanálisis:

			El estudio de técnicas para romper esquemas de encriptación.

			Es fundamental en el diseño de algoritmos robustos.


		9. SSL/TLS (Secure Sockets Layer/Transport Layer Security):

			Protocolos de seguridad utilizados para establecer conexiones seguras en la web, por ejemplo, al realizar transacciones en línea.


		10. Criptografía Cuántica:

			Investigación en el uso de principios cuánticos para mejorar la seguridad y la privacidad en la comunicación.


	La seguridad informática es un campo en constante evolución debido a la creciente sofisticación de las amenazas. 

	La elección de algoritmos y técnicas adecuados depende del contexto y de los requisitos específicos de seguridad de un sistema o aplicación.



|| Algoritmo de Grafos: 

	Son técnicas matemáticas y computacionales utilizadas para analizar y manipular grafos, que son estructuras que modelan relaciones entre entidades.

	Un grafo consiste en un conjunto de nodos (vértices) y un conjunto de aristas (conexiones) que definen las relaciones entre esos nodos.


	Conceptos Fundamentales:

		1. Nodo (Vértice):

			Representa una entidad individual en el grafo.

		2. Arista:

			Conexión entre dos nodos que representa una relación.

		3. Grafo Dirigido:

			Grafo donde las aristas tienen una dirección, es decir, van desde un nodo de origen a un nodo de destino.

		4. Grafo No Dirigido:

			Grafo donde las aristas no tienen dirección, simplemente conectan dos nodos.

		5. Peso de Arista: 

			Valor asociado a una arista que puede representar una medida como distancia, costo, etc



	Algoritmos Básicos:

		1. Recorrido en Profundidad (DFS - Depth-First Search):

			Explora tan lejos como sea posible a lo largo de una rama antes de retroceder. 

			Se implementa a menudo utilizando recursión o una pila.


		2. Recorrido en Anchura (BFS - Breadth-First Search):

			Explora todos los vecinos de un nodo antes de pasar a los vecinos de sus vecinos. 

			Se implementa utilizando una cola.


		3. Algoritmo de Dijkstra:

			Encuentra el camino más corto desde un nodo de origen hasta todos los demás nodos en un grafo ponderado con pesos no negativos.


		4. Algoritmo de Bellman-Ford:

			Encuentra el camino más corto desde un nodo de origen hasta todos los demás nodos en un grafo, incluso si hay aristas con pesos negativos.


		5. Algoritmo de Kruskal:

			Encuentra el árbol de expansión mínima de un grafo no dirigido y conexo. 

			Se utiliza comúnmente en problemas de optimización de redes.


		6. Algoritmo de Prim:

			Encuentra el árbol de expansión mínima de un grafo no dirigido y conexo. 

			Similar a Kruskal, pero con un enfoque diferente.


		7. Orden Topológico:

			En un grafo dirigido acíclico (DAG), encuentra un orden lineal de los nodos de manera que para cada arista dirigida, el nodo de destino aparece después del nodo de origen.



	Problemas Comunes:

		Problema del Camino más Corto:

			Encontrar la ruta más corta entre dos nodos en un grafo ponderado.

		Problema del Ciclo Hamiltoniano:

			Encontrar un ciclo que visite cada nodo exactamente una vez en un grafo no dirigido.

		Problema del Flujo Máximo:

			Determinar la cantidad máxima de flujo que puede pasar desde un nodo fuente hasta un nodo sumidero en un grafo dirigido ponderado.

		Problema del Emparejamiento Máximo:

			Encontrar el conjunto más grande de aristas no adyacentes en un grafo no dirigido.

		Problema de la Coloración de Grafos:

			Asignar colores a los nodos de un grafo de manera que no  haya dos nodos adyacentes del mismo color.


	Son solo algunos ejemplos de los muchos algoritmos y problemas asociados con grafos. 

	La elección del algoritmo depende del tipo de problema y
	las características del grafo en cuestión.



|| Algoritmo de Procesamiento de Imagen y Visión:

	Se utilizan para analizar y manipular imágenes de diversas maneras. 

	Estos algoritmos juegan un papel fundamental en aplicaciones que van desde el reconocimiento de patrones y la detección de objetos hasta la mejora de imágenes y la realidad aumentada


	Conceptos Fundamentales:

		1. Pixeles:

			Los pixeles son los elementos más pequeños de una imagen.

			Cada pixel tiene un valor que representa su intensidad luminosa o de color.


		2. Espacios de Color:

			Representan cómo se codifica y representa el color en una imagen. 

			Ejemplos incluyen RGB (Rojo, Verde, Azul) y HSV (Matiz, Saturación, Valor).


		3. Filtros de Imagen:

			Se utilizan para resaltar o atenuar ciertas características de una imagen.

			Los filtros pueden ser utilizados para suavizar, resaltar bordes, realzar detalles, etc


	Algoritmos de Procesamiento de Imágenes:

		1. Suavizado y Desenfoque:

			Algoritmos como el filtro Gaussiano y el filtro de media se utilizan para reducir el ruido y suavizar la imagen.


		2. Detección de Bordes:

			Algoritmos como el operador Sobel y el detector de bordes de Canny identifican las transiciones de intensidad que indican bordes en la imagen.


		3. Transformaciones Geométricas:

			Incluyen rotación, escala, traslación y deformación de la imagen.


		4. Umbralización:

			Se utiliza para convertir una imagen en una imagen binaria, donde los pixeles se clasifican como blanco o negro según un umbral específico.


		5. Histograma:

			El análisis del histograma permite comprender la distribución de intensidades en una imagen y puede utilizarse para ajustar el contraste.


	Algoritmos de Visión Computacional:

		1. Detección de Características:

			Algoritmos como SIFT (Scale-Invariant Feature Transform) y SURF (Speeded Up Robust Features) encuentran puntos de interés y descripciones que son invariantes a la escala y la rotación.


		2. Emparejamiento de Características:

			Se utiliza para asociar puntos de interés entre dos o más imágenes. 

			El algoritmo RANSAC (Random Sample Consensus) es comúnmente utilizado en este contexto.


		3. Detección de Objetos:

			Algoritmos como Haar Cascade y YOLO (You Only Look Once) se utilizan para detectar objetos específicos en una imagen.


		4. Segmentación de Imágenes:

			Divide una imagen en segmentos más pequeños para facilitar el análisis. 

			Algoritmos de segmentación incluyen el método de k-means y el algoritmo de Watershed.


		5. Reconocimiento de Patrones y Clasificación:

			Se utiliza para asignar una etiqueta a una imagen basada en su contenido. 

			Las redes neuronales convolucionales (CNN) son ampliamente utilizadas en esta tarea.


		6. Realidad Aumentada:

			Combina elementos virtuales con el mundo real a través de la visión de una cámara. 

			Se utilizan algoritmos de seguimiento de marcadores y de estimación de pose.


		7. Reconocimiento Facial:

			Utiliza algoritmos para detectar y reconocer caras en imágenes. 

			Algoritmos como el reconocimiento de eigenfaces y el reconocimiento basado en características locales son comunes.


		8. Estimación de Movimiento:

			Se utiliza para seguir el movimiento de objetos en una secuencia de imágenes. 

			El flujo óptico es un enfoque común para esta tarea.



|| Algoritmo de Análisis de Sentimientos

	Son técnicas utilizadas para determinar la actitud, emoción o tono general expresado en un texto, ya sea en forma de opiniones, reseñas, tweets u otras formas de comunicación escrita. 

	Estos algoritmos son comúnmente utilizados en el procesamiento del lenguaje natural (PLN) y en aplicaciones de minería de opiniones para comprender la opinión de usuarios sobre productos, servicios o eventos.


	Enfoques para el Análisis de Sentimientos:

		1. Basado en Reglas:

			Utiliza reglas gramaticales y léxicas para determinar la polaridad de las palabras y la estructura de las oraciones.

			Puede ser efectivo pero puede carecer de sutileza para abordar la complejidad del lenguaje natural.


		2. Basado en Diccionarios de Sentimientos:

			Asocia palabras con valores de polaridad (positiva, negativa o neutral) mediante el uso de diccionarios específicos de sentimientos. 

			Cada palabra contribuye a una puntuación general.


		3. Aprendizaje Supervisado:

			Utiliza modelos de aprendizaje automático entrenados en conjuntos de datos etiquetados con sentimientos.

			Algoritmos como Support Vector Machines (SVM), Naive Bayes y clasificadores basados en árboles de decisión se utilizan comúnmente.


		4. Aprendizaje No Supervisado:

			Agrupa documentos o frases en categorías de sentimientos sin el uso de etiquetas previas. 
		
			El análisis de tópicos y la técnica de agrupamiento pueden ser útiles en este enfoque.


		5. Redes Neuronales:

			Las redes neuronales, especialmente las recurrentes (RNN) y las redes neuronales transformadoras (BERT), han demostrado ser eficaces en tareas de análisis de sentimientos, ya que pueden capturar contextos complejos y dependencias a largo plazo en el lenguaje



	Etapas del Análisis de Sentimientos:

		1. Preprocesamiento del Texto:

			Incluye la eliminación de stop words, la lematización, la tokenización y otras técnicas para preparar el texto antes del análisis.


		2. Extracción de Características:

			Transforma el texto en características numéricas que los modelos de aprendizaje automático pueden entender.

			Esto puede implicar el uso de representaciones vectoriales como TF-IDF o embeddings.


		3. Modelado:

			Utiliza un modelo (como SVM, Naive Bayes, LSTM, BERT, etc.) para aprender patrones en los datos de entrenamiento y realizar predicciones sobre nuevos textos.


		4. Evaluación y Ajuste:

			Evalúa el rendimiento del modelo utilizando métricas como precisión, recall, F1-score, etc. Luego, ajusta el modelo según sea necesario


	Desafíos y Consideraciones:

		1. Sarcasmo y Ironía:

			La detección de sarcasmo e ironía puede ser difícil, ya que el significado real puede diferir del significado literal.


		2. Contexto Cultural y Lingüístico:

			La comprensión de ciertos giros lingüísticos y expresiones puede variar según el contexto cultural y regional.


		3. Ambigüedad:

			Algunas frases pueden ser ambiguas y tener múltiples interpretaciones, lo que dificulta la clasificación precisa.


		4. Cambios en el Significado:

			El significado de algunas palabras puede cambiar dependiendo del contexto en el que se utilicen.


	El análisis de sentimientos es una área activa de investigación
	y desarrollo en procesamiento del lenguaje natural, y los avances en técnicas de aprendizaje profundo han mejorado significativamente la capacidad de estos algoritmos para comprender el lenguaje humano de manera más sutil y precisa.



|| Algoritmo de Routing: 

	Los algoritmos de enrutamiento, también conocidos como algoritmos de enrutamiento de red, son utilizados en redes de computadoras para determinar la mejor ruta para  transmitir datos desde el origen hasta el destino a través de una red de nodos interconectados. 

	El objetivo principal de estos algoritmos es optimizar la eficiencia y la confiabilidad del transporte de datos.

	Hay varios enfoques y algoritmos para lograr esto, dependiendo de la topología de la red, los requisitos de rendimiento y otros factores.


	Algoritmos de Enrutamiento:

		1. Enrutamiento Estático:

			Las rutas se configuran manualmente y no cambian automáticamente con las condiciones de la red. 

			Es simple pero menos adaptable a cambios en la topología o carga de la red.


		2. Enrutamiento Dinámico:

			Los algoritmos de enrutamiento dinámico ajustan automáticamente las rutas en función de las condiciones de la red. 

			Estos algoritmos son más flexibles y reactivos a cambios.



	Algoritmos de Enrutamiento en Redes de Área Local (LAN):

		1. Algoritmo de Enrutamiento de Vector de Distancia (Distance Vector Routing):

			Cada nodo mantiene una tabla que contiene la distancia a todos los demás nodos en la red. 

			El enrutador elige la ruta con la menor distancia. 

			Ejemplos incluyen RIP (Routing Information Protocol).


		2. Algoritmo de Estado de Enlace (Link State Routing):

			Los nodos intercambian información sobre el estado de sus enlaces y construyen un mapa completo de la red. 

			Utilizando este mapa, cada nodo calcula la mejor ruta hacia cada destino. 

			Ejemplos incluyen OSPF (Open Shortest Path First) y IS-IS (Intermediate System to Intermediate System).


	Algoritmos de Enrutamiento en Redes de Área Amplia (WAN):

		1. BGP (Border Gateway Protocol):

			Utilizado en el nivel de Internet para intercambiar información entre sistemas autónomos (AS). 

			BGP toma en cuenta factores políticos y de costo en la toma de decisiones de enrutamiento.


		2. EIGRP (Enhanced Interior Gateway Routing Protocol):

			Desarrollado por Cisco, EIGRP combina elementos de enrutamiento de vector de distancia y estado de enlace. 

			Es específico para redes de Cisco.



	Algoritmos de Enrutamiento sin Conexión:

		1. Algoritmo de Enrutamiento de Distancia Más Corta (Shortest Path Routing):

			Utilizado en la capa de enlace de datos para encontrar la ruta más corta hacia un destino. 

			El algoritmo de Dijkstra es comúnmente utilizado.


		2. Enrutamiento por Salto (Hop-by-Hop Routing):

			Cada nodo toma decisiones de enrutamiento basadas en la información local y pasa el paquete al siguiente nodo en el camino hacia el destino



	Protocolos de Enrutamiento para Redes Ad Hoc:

		1. AODV (Ad Hoc On-Demand Distance Vector):

			Utilizado en redes ad hoc, donde los nodos se comunican directamente entre sí sin la necesidad de una infraestructura de red preexistente.


		2. DSR (Dynamic Source Routing):

			Otro protocolo para redes ad hoc que permite a los nodos descubrir rutas dinámicamente.


	Consideraciones y Desafíos:

		1. Convergencia:

			El tiempo necesario para que los enrutadores converjan a una nueva configuración después de un cambio en la red.


		2. Escalabilidad:

			La capacidad del algoritmo de enrutamiento para manejar grandes redes y crecimiento futuro.


		3. Tolerancia a Fallos:

			La capacidad del sistema de continuar funcionando correctamente incluso cuando algunos nodos o enlaces fallan.


		4. Optimización de Rutas:

			La elección de rutas basada en criterios como el menor costo, menor latencia, etc.


		5. Seguridad:

			La implementación de medidas para proteger la información de enrutamiento y prevenir ataques maliciosos.
