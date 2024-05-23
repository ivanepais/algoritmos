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



|| Análisis de Algoritmos

	Es una rama de las ciencias de la computación que estudia el rendimiento de los algoritmos, especialmente su tiempo de ejecución y requerimientos de espacio.

	El objetivo práctico del análisis de algoritmos es predecir el rendimiento de diferentes algoritmos con el fin de guiar decisiones de diseño.

	Por ejemplo, responder "la manera más eficiente para ordenar un millón de enteros de 32 bit."

	Usando el ordenamiento de burbuja (bubble sort) o el ordenamiento radix. 

	El ordenamiento de burbuja es simple pero lento para bases de datos grandes. 

	El ordenamiento radix que es muy rapido y eficiente cuando se trata de ordenar linealmente grandes grupos de números cortos pero no funciona tan bien con números extensos.  



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
	

|| Árbol AVL


|| Heap


|| Grafo




|| Algoritmos de Optimización y Programación Dinámica


    1. Algoritmos de Optimización

        Algoritmo de Dijkstra.
        Algoritmo de Bellman-Ford.


    2. Programación Dinámica

        Principios de la programación dinámica.

        Problemas clásicos (Fibonacci, Knapsack, Longest Common Subsequence).



|| Algoritmos Avanzados

	1. Algoritmos de Dividir y Vencerás y Greedy:

    	Dividir y Vencerás:
        	
        	Principios y ejemplos (Merge Sort, Quick Sort).


    	Algoritmos Greedy:
        	
        	Principios de algoritmos voraces.
        	
        	Problemas clásicos (Huffman Coding, Activity Selection).