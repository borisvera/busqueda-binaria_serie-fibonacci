
========================================================================================================
= Busqueda binaria: logaritmica
========================================================================================================

El algoritmo de búsqueda binaria divide el tamaño de la lista por 2 hasta quedarse con una lista de tamaño 1.
Al llegar al tamaño unitario se puede determinar directamente si el elemento buscado existe o no.



número de | tamaño de
iteración | lista  
-------------------------------   
		  | 		  1
   1	  |		   n/2
-------------------------------
		  |			  2	
   2	  |		   n/2
-------------------------------
		  |			  3	
   3	  |		   n/2
-------------------------------
		.....
		  |			  t	
   t	  |		   n/2
-------------------------------

La division de sublistas requiere t iteraciones, en cada iteración el tamaño de la sublista se reduce a la mitad
La sucesión de tamaños de las sublistas hasta una sublista de longitud 1, entonces:

	  t	
   n/2   = 1
   
Tomando logaritmos en base 2 en la expresión anterior quedará:
		 t
	n = 2

 log n = t
	2
Por esa razón la complejidad del caso peor es O(log n).

	

	
========================================================================================================
= Serie Fibonacci: exponencial
========================================================================================================

Tenemos la siguiente serie de Fibonacci:

1, 1, 2, 3, 5, 8, ...

La serie empieza con 1, 1, y los siguientes elementos son la suma de los dos anteriores.
Una forma muy simple de generar el elemento n de esta serie es:

	i es tres
	elemento uno es uno
	elemento dos es uno
	bucle que para cuando i es igual a n
	elemento i es elemento i-1 más elemento i-2



La función fibonacci que requiere el número de elemento a ser calculado (n)
si el elemento es uno o dos, devolver el valor uno
de lo contrario el resultado es el dado por la suma de la función fibonacci de los elementos n y n-1

Es decir, para calcular un elemento llamamos a la misma función dos veces. Cada una de dichas funciones se llama a si misma otras dos veces, etc. Es decir, crece exponencialmente.


paso 1: 2 ejecuciones
paso 2: 2* (2 ejecucuciones)
paso 3: 2*(2*(2 ejecuciones))
paso k: (2^k) ejecuciones



