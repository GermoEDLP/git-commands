

 1. git init										--> Inicializar repositorio
		git config --global user.name "German" 			--> Configurar el nombre
		git config --global user.email "ger@gmail.com" 	--> Configurar el mail

 2. git add 
		git add prueba.html 	--> Empezar a seguir al archivo prueba.html
		git add css/ 			--> Empezar a seguir la carpeta css
		git add css/*.css	--> Empezar a seguir todos os archivos extensión .css dentro de la carpeta css
		git add .				--> Seguir todo
		git add -A			--> Seguir todo
		git add --all			--> Seguir todo

 3. git commit 										--> Trabajar con las fotos que le hacemos al stage
													Si escribimos esto unicamente, nos abre el editor VIM => 	i	-> Empezar a escribir
																											Esc -> Salir del modo escritura
																											:wq -> Salir y guardar
		git commit -m "Mensaje"						--> Sacar una foto y colocar un mensaje de que cambios se realzaron desde la foto anterior
		git commit --amend -m "Mensaje corregido"		--> Corregir el mensaje del ultimo commit

 4. git status		--> Nos informa en que rama estamos y en que estado estan los archivos que seguimos, si estan actualizados o no.

 5. git show							--> Muestra los cambios entre commits
		git show [nombreDelTag]		--> Muestra los cambios dentro de esa etiqueta

 6. git diff							--> Nos muestra la diferencia entre el estado actual y la foto anterior
		git diff prueba.html			--> Nos muestra la diferencia entre el estado actual y la foto anterior pero solamnete del archivo prueba.html

 7. git checkout [comandos]			--> Trabajamos con los tiempos de las fotos y las ramas.
		git checkout .				--> Volvemos todos los cambios a la foto anterior.
		git checkout -- prueba.html	--> Volvemos los cambios a la foto anterior del archivo prueba.html solamente
		git checkout nuevaRama		--> Me muevo a la rama nuevaRama
		git checkout -b nuevaRama	--> Crea la rama nuevaRama y me dirije a ella
	
 8. git log								--> Muestra el historico de los commits realizados
		git log --online --decorate --all --graph 	--> Muestra el historico de los commits realizados pero con mas detalle y en mejor formato

 9. git reset [comandos]				--> Deja de seguir los archivos que le expecifiques o vuelve a un punto expecifico del tiempo
		git reset prueba.html 			--> Deja de seguir al archivo prueba.html
		git reset css/ 					--> Deja de seguir la carpeta css
		git reset css/*.css				--> Deja de seguir todos os archivos extensión .css dentro de la carpeta css
		git reset .						--> deja de seguir todo
		git reset --soft [commitNumber]	--> Vuelve al commit que se indica pero no recupera archivos, solo veo los cambios
		git reset --hard [commitNumber]	--> Vuelve al commit que se indica y recupera archivos.

 10. git config --global alias.[aliasElegido] "[comando]" 	--> Cambia el uso del comando por el del alias elegido
		git config --global alias.s "status"					--> Ahora el 'git status' puede ponerse como 'git s' 

 11. git mv nombreOriginal.html nuevoNombre.html		--> Cambiar el nombre de un archivo y dejar constancia en un commit

 12. git rm archivoABorrar.html						--> Borrar un archivo y dejar constancia en un commit

 13. git reflog		--> Veo un historial de commit que incluyen aquellos reseteados.

 14. git branch 						--> Trabajar con ramas
		git branch nuevaRama		--> Crear rama nuevaRama
		git branch -d nuevaRama		--> Borrar la nuevRama

 15. git merge						--> unir ramas de trabajo
		git merge nuevaRama		--> Estando en la rama principal, la uno con la rama nuevaRama

 16. git tag [comandos]										--> Manejo de etiquetas para versionar
		git tag												--> Ver en la etiqueta que estamos trabajando
		git tag version1										--> Se crea la etiqueta version1 y se le coloca a la rama que estemos trabajando
		git tag -d version1									--> Borra la etiqueta versión1
		git tag -a v1.0.0 -m "Mensaje"							--> Se le da a la etiqueta una version y se le coloca un mensaje que explica que es
		git tag -a v0.0.1 [commitNumber]  -m "Mensaje"			--> Se le da a la etiqueta una version y se le coloca un mensaje que explica que es en el commit expecificado no importa en que parte del historial esta
		
 17. git clone [URLGitHub]											--> Clona un repositorio que esta en GitHub

 18. git push														--> Sube al repositorio que esta en GitHub y que definimos como remoto los commits realizados
		git push origin master									--> Sube al repositorio que esta en GitHub y que definimos como remoto los commits realizados en la rama master del oroginal, si trabajamos desde un 'git clone', los cambios se reflejarán igual.

 19. git pull 														--> Traer los cambios que esten en GitHub, pero que no esten en tu repositorio local. Es decir, si hay algun cambio en tu repositorio virtual que no se reflejan en tu repositorio local, este comando los empareja.

 19. git fetch 													--> Igual al 'git pull' pero no hace el merge automaticamnete, sino que debemos hacerlo manualmente.

