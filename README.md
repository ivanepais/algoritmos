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

	



|| Análisis de Algoritmos

	Es una rama de las ciencias de la computación que estudia el rendimiento de los algoritmos, especialmente su tiempo de ejecución y requerimientos de espacio.

	El objetivo práctico del análisis de algoritmos es predecir el rendimiento de diferentes algoritmos con el fin de guiar decisiones de diseño.

	Por ejemplo, responder "la manera más eficiente para ordenar un millón de enteros de 32 bit."

	Usando el ordenamiento de burbuja (bubble sort) o el ordenamiento radix. 

	El ordenamiento de burbuja es simple pero lento para bases de datos grandes. 

	El ordenamiento radix que es muy rapido y eficiente cuando se trata de ordenar linealmente grandes grupos de números cortos pero no funciona tan bien con números extensos.  




|| Algoritmos Básicos

	1. Algoritmos de Ordenación:

	    Bubble Sort, Selection Sort, Insertion Sort.

	    Merge Sort, Quick Sort.


	2. Algoritmos de Búsqueda:

	    Búsqueda lineal.

	    Búsqueda binaria.



|| Algoritmos y Estructuras de Datos Avanzadas

	
	1. Recorridos de Grafos:

    	BFS (Breadth-First Search).
    	
    	DFS (Depth-First Search).	


    2. Estructuras de Datos Avanzadas:

    	Árboles binarios.
    	
    	Árboles AVL.
    	
    	Heaps.



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