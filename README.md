# algo2-tp2
Algoritmos 2 - TP2

## Lista de cosas para hacer

[X] Mover

[X] Conectar

[X] Desconectar

[X] Agregar pokemon!!

[X] Esa funcion que te da un vector con los jugadores del pokenodo

[X] Rep de Juego castellano

[X] Rep de Juego logica

[X] Terminar auxiliares del rep de Juego
 
[X] Abs de Juego

[ ] Revisar Conectar y Desconectar (igual creo que están bien, pero por las dudas)

[X] Agregar Copiar() en mapa  (No hacia falta)

[ ] REVISAR ALLIASING Y ALIAS!!!!!!!!!!!!!!!!! (sobre todo en heap)

[X] Revisar como borrar un nodo y acomodar iteradores en la funcion borrar del iterador del heap

[ ] Los "hayPadre", "hijoderecho" etc no tienen que estar en la interfaz del heap

[ ] Hacer la funcion publica "HaySiguiente" y "Siguiente" para acceder al elemento del heap

[X] Revisar si hace falta de verdad iteradores de heap, capaz con punteros funca, no se

[ ] Arreglar interfaz de Juego incompletas (pre, post, complejidad)

[X] Justificar algoritmos de heap

[ ] Revisar 40 veces los algoritmos del heap

[ ] Agregar Copiar() en heap

[ ] Retocar el heap (complejidades, justificaciones, etc)

[X] Desencolar de heap

[X] Ver complejidad de AgregarCoordenada en mapa

[ ] Para asignar a un puntero algo que no es un puntero hay que usar &. Ver AgregarPokemon, estado 18

[ ] Revisar PosPokemonCercano y HayPokemonCercano, porque creo que esta mal eso de revisar coordenadas sumando y restando 1.
Se supone que no me importa como estan hechas las coordenadas, en teoria no tengo forma de saber que la de la derecha es +1,
porque de como esta implementada se encarga el mapa. Deberia usar las funciones "coordenadaALaDerecha" o esas de mapa.

[ ] Hay siguiente de iteradores de heap

[X] Preguntar lo de MultiConjunto. Es necesario hacer el modulo? ver .txt de preguntas para mas info

[X] Rep de Trie

[X] Abs de Trie

[ ] Rep Heap

[ ] Abs Heap

[X] Agregar en el rep de juego que no puede haber repetidos entre los elementos que capturo el jugador.
jonathan: Ya no es necesario porque ahora usamos un diccionario

[X] Actualizar estructura: ahora existen posConPokemons que es una lista de coordenadas, y reemplaza la lista de pokemons del jugador, por un trie de pokemons - cantidad

[ ] Iterador de funcion pokemons, es un iterador modificado de conjunto (despues de todo quiero que recorra las claves del conjunto) lo unico que modifica el es "siguiente" que me da el significado como tuplas ?

[X] Revisar rep y abs para la nueva estructura

[X] Modificar agregarPokemon para que actualice las posConPokemons

[X] Algoritmos de Heap

[ ] Los demas algoritmos de Juego

[X] Interfaz de las funciones que exporta coordenada (derecha, izquierda ..)

[X] Algoritmos de las funciones que exporta coordenada (derecha, izquierda ..)

[X] GrillaJugs deberia ser vector(vector(jugador)) (nat en vez del jugstruc) Cambiarlo y revisar los algoritmos que usan la grilla para ver que no rompemos nada

[X] !!! Hacer iterador para recorrer el vector de jugadores. Lo tenemos que hacer nosotros porque necesitamos que se saltee los eliminados!!!
- jonathan: solucion alternativa, mantener actualizado un conjunto de jugadores no eliminado. Voy a tener que modificar la estructura un poco.

[ ] Renombrar heap por colaDePrioridad donde corresponda

[X] Explicacion de estructura para Juego

[X] Explicacion de estructura para Mapa

[X] Explicacion de estructura para Trie

[ ] Explicacion de estructura para Heap

[ ] Buscar algun checklist de diseño y ver que falta

[X] Renombrar los usos de diccTrie

[ ] Renombrar los usos de Heap

[X] Funcion CrearGrilla(tam) en Mapa. Tiene que ser privada, no aparece en la interfaz pero falta el algoritmo

[ ] Revisar justificaciones de complejidades

[ ] Informe

[X] Arreglar algunas funciones viejas que estan todo en modo matematico

lo haria pero se que hay cosas mas importantes -jonathan
[ ] En modulo Mapa, reemplazar vectores por arreglos, para que las complejidades sean mas limpias

[ ] Rezar no equivocarse
