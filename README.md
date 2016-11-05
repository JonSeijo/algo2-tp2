# algo2-tp2
Algoritmos 2 - TP2

## Lista de cosas para el recu

[X] Estructura de nuevoHeap

[X] Algoritmos de heap

[X] Rep de Heap (en castellano)

[X] Abs de heap

[X] Hay un error cuando busco el siguiente ultimo. Lo arreglo despues

[ ] Iterador

[ ] Borrar de iterador

[ ] Revisar rep de juego

[ ] Revisar aliasing

[ ] Rezar no equivocarse

-----
Página 20 Entrenadores Posibles: REVISAR el algoritmo, hay cosas raras, en un momentos hacemos un puntero que después no usamos y hay un Avanzar de un vector pero que ya está siendo recorrido por un for, no me termina de cerrar bien.

-----
Revisar del Heap:

[ ] Definir el "<" para las tuplas <jugador, cant atrapados> 

[ ] En muchos lados: un nodo no es un puntero a nodo, cuando asigno a un puntero deberia usar &
	Por ejemplo:   (nodo → izq) ← &(nuevoNodo)    o algo asi

[ ] Arreglar todas las funcioens privadas porque las pre y post se ven mal, seguir el modelo del trie

[ ] Encolar:
	[X] Debería ser in/out
	[X] Línea 3 y 6: "c.raiz <- nuevoNodo" c.raiz es un puntero a nodo, y nuevoNodo es un nodo. Estamos asignando un nodo a un puntero a nodo, ¿hay que cambiarlo o así está bien? Está en varias funciones esto.
	[X] Línea 15: ¿No debería ser "(c.ultimo -> padre -> DER)"?
	[X] Esto hay que cambiarlo porque no cubre todos los casos, ponele un heap de altura 4, donde los tres primeros niveles están completos (yendo de arriba para abajo deberían tener 1, 2 y 4 nodos) y en el último hay 4 nodos exactamente. Cuando hay que agregar un nuevo nodo, para encontrar el último hay que subir hasta que algún nodo "n" sea hijo izquierdo, pasar al hijo derecho del padre de n y bajar por la izquierda hasta llegar a NULL, y ahí agregar el nuevo. Esto funciona siempre que el último sea un hijo derecho, el último nivel del heap no esté completo y hay que buscar un nuevo "ultimo".

[ ] Desencolar:
	[ ] Debería ser in/out
	[ ] Línea 1: Lo mismo que en la linea 3 de Encolar, a la función auxiliar SwapNodo le estamos pasando punteros y en la aridad dice que recibe nodos (también pasa en la función swapConHijos)

[ ] SwapNodos: hay que asignar el nuevo "ultimo" del heap en caso de swapear este (en linea 10 y 13 comparamos punteros a nodos con nodos)

[ ] SwapConmHijoIzqi: En la línea 4 no debería ser "(a -> der -> padre) <- a"
		      En la linea 7 no debería ser "(b -> der -> padre) <- b"
			Marea pero hay que fijarse que antes de esas lineas a->der y b->der ya fueron asignados, entonces no son los mismos con los que arranca el heap

[ ] SwapConHijoDER: En la línea 4 no debería ser "(a -> izq -> padre) <- a"
		      En la linea 8 no debería ser "(b -> izq -> padre) <- b"

[ ] Hacer Eshijoizq? Eshijoder? PERO OJO, que pasa si es raíz? debería dar falso en ambos casos, dentro de estas funciones comprobar que no sea NULL antes de preguntar nada así no se indefine


[ ] SiftUP: En la guarda del while no debería haber un "^luego" en vez de un "^" ?, tampoco se le pasa el heap como parámetro y habría que tenerlo para los swaps, recibe un nodo y no un puntero, cuando se hace el llamada de la función se le pasa un puntero (esto último también pasa con siftdown)
----
(Esperar a correccion de tp, es un bardo cambiar esto y si no estaba mal joya)
jonathan: Nos marcaron que estaba bien asi que esto no lo cambio
[-] Revisar PosPokemonCercano y HayPokemonCercano, porque creo que esta mal eso de revisar coordenadas sumando y restando 1.
Se supone que no me importa como estan hechas las coordenadas, en teoria no tengo forma de saber que la de la derecha es +1,
porque de como esta implementada se encarga el mapa. Deberia usar las funciones "coordenadaALaDerecha" o esas de mapa.
