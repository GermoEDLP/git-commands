# Repositorio de información sobre Comandos de Git

1. ### Inicialización

	* __config:__ Ayuda a la configuración de las variables de entorno
		* Configurar el nombre:
		~~~
		git config --global user.name "German"
		~~~
		*  Configurar el email: 
		~~~
		git config --global user.email "test@test.com"
		~~~
	* __init:__ Inicializa un repositorio nuevo reinicializa uno existente
		~~~
		git init
		~~~

2. ### Stage
	Para llevar algo al stage debemos utilizar el comando `add`:

	* Empezar a seguir al archivo prueba.html
	~~~
	git add prueba.html 	
	~~~
	* Empezar a seguir la carpeta css
	~~~
	git add css/ 			
	~~~
	* Empezar a seguir todos os archivos extensión .css dentro de la carpeta css
	~~~
	git add css/*.css	
	~~~
	* Seguir todo
	~~~
	git add .				
	~~~
	* Seguir todo
	~~~
	git add -A			
	~~~
	* Seguir todo
	~~~
	git add --all			
	~~~

3. ### Snapshot
	Para tomar una fotografia de la información en el stage, usaremos el comando `commit`

	* Sacar una foto y colocar un mensaje de que cambios se realzaron desde la foto anterior
	~~~
	git commit -m "Mensaje"
	~~~				
	* Corregir el mensaje del ultimo commit
	~~~
	git commit --amend -m "Mensaje corregido"
	~~~
	* Si escribimos unicamente el comando `commit`, nos abre el editor VIM. Este editor se comanda utilizando:
		* __i -->__ Empezar a escribir
		* __Esc -->__ Salir de modo lectura
		* __:wq -->__ Salir y guardar
	~~~
	git commit
	~~~

4. ### Estado
	
	* __status:__ Nos informa el estado de la aplicaicón asi como la rama, los seguimientos y el usuario
	~~~
	git status
	~~~
	* Si queremos que sea un poco mas limpia la información
	~~~
	git status -s
	~~~
	* Si queremos que ademas de ser mas limpia, nos muestre la rama en al que estamos 
	~~~
	git status -s -b
	~~~