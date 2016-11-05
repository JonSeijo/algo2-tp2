# algo2-tp2
Algoritmos 2 - TP2

## Lista de cosas para el recu

[X] Estructura de nuevoHeap

[X] Algoritmos de heap

[X] Rep de Heap (en castellano)

[X] Abs de heap

[X] Hay un error cuando busco el siguiente ultimo. Lo arreglo despues

[X] Iterador

[ ] Borrar de iterador

[X] Siguiente de iterador

[ ] Revisar rep de juego

[ ] Revisar aliasing

[ ] Rezar no equivocarse

-----
Página 20 Entrenadores Posibles: REVISAR el algoritmo, hay cosas raras, en un momentos hacemos un puntero que después no usamos y hay un Avanzar de un vector pero que ya está siendo recorrido por un for, no me termina de cerrar bien.

-----
Revisar del Heap:

[ ] Definir el "<" para las tuplas <jugador, cant atrapados> 

[X] En muchos lados: un nodo no es un puntero a nodo, cuando asigno a un puntero deberia usar &
	Por ejemplo:   (nodo → izq) ← &(nuevoNodo)    o algo asi
jonathan: creo que el problema solo estaba en el Encolar

[X] Arreglar todas las funciones privadas porque las pre y post se ven mal

[X] Encolar:

	[X] Debería ser in/out

	[X] Línea 3 y 6: "c.raiz <- nuevoNodo" c.raiz es un puntero a nodo, y nuevoNodo es un nodo. Estamos asignando un nodo a un puntero a nodo, ¿hay que cambiarlo o así está bien? Está en varias funciones esto.

	[X] Línea 15: ¿No debería ser "(c.ultimo -> padre -> DER)"?

	[X] Esto hay que cambiarlo porque no cubre todos los casos, ponele un heap de altura 4, donde los tres primeros niveles están completos (yendo de arriba para abajo deberían tener 1, 2 y 4 nodos) y en el último hay 4 nodos exactamente. Cuando hay que agregar un nuevo nodo, para encontrar el último hay que subir hasta que algún nodo "n" sea hijo izquierdo, pasar al hijo derecho del padre de n y bajar por la izquierda hasta llegar a NULL, y ahí agregar el nuevo. Esto funciona siempre que el último sea un hijo derecho, el último nivel del heap no esté completo y hay que buscar un nuevo "ultimo".

[X] Desencolar:
	[X] Debería ser in/out
	[X] Línea 1: Lo mismo que en la linea 3 de Encolar, a la función auxiliar SwapNodo le estamos pasando punteros y en la aridad dice que recibe nodos (también pasa en la función swapConHijos)

[ ]
jonathan:
En SwapNodos estaria pasando lo mismo que nos corrigieron en el trie, estamos asignando a un puntero un nodo que entra por parametros. 
Como es privada creo que basta con que chequeemos que no lo usamos mal ni rompemos nada. Si usamos "copiar" es una mierda porque podriamos estar copiando el heap entero (el nodo que pasan por parametros puede ser la raiz por ejemplo) y eso es O(n)
Tenemos que consultarlo, para mi esta bien como esta ahora si es que chequeamos que no lo rompemos en otro lado (porque es privada)




[X] SwapNodos: hay que asignar el nuevo "ultimo" del heap en caso de swapear este 

[X] en linea 10 y 13 comparamos punteros a nodos con nodos

[X] SwapConmHijoIzqi: En la línea 4 no debería ser "(a -> der -> padre) <- a"
		      En la linea 7 no debería ser "(b -> der -> padre) <- b"
			Marea pero hay que fijarse que antes de esas lineas a->der y b->der ya fueron asignados, entonces no son los mismos con los que arranca el heap

[X] SwapConHijoDER: En la línea 4 no debería ser "(a -> izq -> padre) <- a"
		      En la linea 8 no debería ser "(b -> izq -> padre) <- b"

[X] Hacer Eshijoizq? Eshijoder? PERO OJO, que pasa si es raíz? debería dar falso en ambos casos, dentro de estas funciones comprobar que no sea NULL antes de preguntar nada así no se indefine

jonathan: creo que por defecto siempre es yluego en programacion, podriamos chusmear otros ejemplos/preguntar

[-] SiftUp: En la guarda del while no debería haber un "^luego" en vez de un "^" ?, 

[X] se le pasa el heap como parámetro y habría que tenerlo para los swaps, 

[X] recibe un nodo y no un puntero, cuando se hace el llamada de la función se le pasa un puntero (esto último también pasa con siftdown)

[X] EsMenorNodos: corrige uso, se le pasaban punteros en vez de nodos


Correcciones marcadas:

[X] Rep de mapa

[ ] PosExistente de mapa.     
jonathan: lo revise y me parece que es un error del corrector. Estoy bastante seguro que nuestra funcion esta bien: consultar

[ ] Referencias en punteros (Definir) de diccString

[X] Error en complejidad en interfaz de Juego: AgregarPokemon

[ ] Revisar CasoMov3 == en condicional

[ ] Revisar CasoMov5 == en condicional

[ ] EntrenadoresPosibles: Revisar algoritmo bien bien

[ ] Expulsados esta repetida


#### SI HAY TIEMPO:

[ ]	Modulo "Matriz" renombre de vector(vector(a)) jeje <- JAJAJAJJAJA

#### Otros
----
(Esperar a correccion de tp, es un bardo cambiar esto y si no estaba mal joya)
jonathan: Nos marcaron que estaba bien asi que esto no lo cambio
[-] Revisar PosPokemonCercano y HayPokemonCercano, porque creo que esta mal eso de revisar coordenadas sumando y restando 1.
Se supone que no me importa como estan hechas las coordenadas, en teoria no tengo forma de saber que la de la derecha es +1,
porque de como esta implementada se encarga el mapa. Deberia usar las funciones "coordenadaALaDerecha" o esas de mapa.
