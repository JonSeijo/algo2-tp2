# algo2-tp2
Algoritmos 2 - TP2

Si quieren hacer un update de enunciado, ponganle nombre de version asi no nos confundimos. Despues revisen en el repo a ver si se actualizo realmente.

Los .pdf estan el el .gitignore, asi que tienen que usar -f cuando hacen el add (o si quieren hacerlo a manopla: quitar al pdf del gitignore, agregar, pushear y despues volver a poner el gitignore original)

###Pasos para actualizar un .pdf

git pull
git rm archivo_viejo
git add archivo_nuevo_1.x -f
git commit -m "Update a version 1.x"
git push
