# PPS-Unidad0Actividad4-JoseMi
===
Vamos a hacer una nueva actividad con git. En esta ocasión crearemos un pequeño proyecto de una página web que podremos visualizar creando un pequeño servidor con php.
Como en la actividad anterior el producto a realizar será el repositorio en github. Allí tendrás que documentar la realización de la práctica con la explicación del procedimiento, sus imágenes, etc.

## Seguimos configurando Fit

Ya habrás configurado tu email y tu user con git config. Vamos a configurar algunas cosas más.

1. Configura el editor de comandos. Yo por simplicidad utilizaría nano ``git config — global core.editor nano``
2. Vamos también a configurar para que cuando utilicemos ``git dif`` o ``git log`` se nos muestre todo el mensaje sin entrar en editor. Para ello git config — global core.pager ' ' ``.
3. Comprueba qué valor tienen las variables de configuración de git. Puedes utilizar la ayuda ``git config --help``.
4. Ajusta los valores de las  variables de git:

~~~
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
~~~ 

## Creación de Proyecto y repositorio

Para ello crea una nueva carpeta en tu directorio de git de PPS, con el nombre de esta actividad ___PPS-Unidad0Actividad4-TuNombre___

Crea un nuevo repositorio público con nombre __PPS-Unidad0Actividad4-TuNombre__

Sigue las indicaciones de github para crear tu nuevo repositorio en linea de comandos, esto es:

![](images/creaRepo.png)

Viene a ser como esto, pero cambiando el nombre de usuario y de repositorio:

~~~
echo "# PPS-Unidad0Actividad4-JoseMi" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:jmmedinac03vjp/PPS-Unidad0Actividad4-JoseMi.git
git push -u origin main
~~~
---
## Iniciando Proyecto 

1. Haz un listado en forma de arbol (tree -a) de todos los archivos del directorio.
2. Crea un archivo con nombre README (si no existe todavía) y lo añades al proyecto.
3. Comprueba el estado de git (``git status``) -s o git status --short. 
4. Escribe en él una descripción de la actividad y vuelves a comprobar su estado.

## Ignorando archivos

1. Crea una carpeta con nombre Excluded. En ella vamos a colocar la documentación que no queremos que sea rastreada y subida al repositorio.
2. Para comprobar que funciona crea algún archivo vacío allí y también crea un archivo con nombre excluido.txt en el directorio principal del repositorio.
3. Crea un archivo .gitignore en el cual vamos a poner que no queremos que se rastreen los archivos con extensión .txt y el directorio Excluded que hemos creado antes.
4. Comprueba el estado del proyecto y comprueba que no nos indica nada del seguimiento de dichos archivos

## Trabajo con git

5. Crea un archivo con nombre index.php. 
6. Introduce el código html para que nos muestre un mensaje de Hola mundo con tu nombre. Uno sencillo sería este:

   ``<H1>Hola $USER¡¡¡ ¿Qué tal te encuentras?</H1>``
   
8. Visualiza el estado del proyecto ( puedes hacer tambien un git status corto ``git status -s`` o ``git status --short``). 
9. Puedes ver como te indica que tienes varias operaciones por hacer: git add, git commit...
1. Añade el archivo index.php al proyecto (git add).
1. Haz un commit.
1. Vuelve a comprobar el estado del proyecto. Puedes ver como ya debería de estar todo en orden.
1. Vuelve a subir los cambios a tu repositorio de github (git push)

## Creación de nuestro servidor web y visualización de nuestro proyecto

1. En un nueva pestaña de terminal y en el mismo directorio, ejecuta php -S 0:8080 para lanzar un servidor con la página html que has creado.
2. Visualiza la página creada Puedes acceder a ella en tu navegador en el puerto 8080 de tu equipo: [](http://localhost:8080)

## Seguimos con el Trabajo con git

1. Haz una copia del archivo local index.php y con el nombre index.php.save. Modifica el fichero index.php para que cambie el texto mostrado en la página web.
2. Verifica estado del proyecto.
3. Comprueba las diferencias de los archivos que no han sido añadidos (``git diff``)
4. Refresca navegador para comprobar que ha cambiado el contenido de nuestra página web.
5. Vuelve a la versión anterior del archivo index.php (git restore).
6. Vuelve a refrescar navegador para ver como vuelve a versión inicial.
7. Utiliza el comando ``git mv``para sobreescribir el archivo index.html con index.html.save
8. Mira el estado del proyecto y confirma todos los cambios.
9. Para pull y push, haz un push y comprueba cómo han subido los archivos a github.com.
1. Modifica el archivo index.php desde la página de github.com y haz un pull y comprueba cómo se ha modificado la página web en nuestro navegador.


## Ramas

1. Lista las ramas existentes.
2. Crea una nueva rama con nombre Vers1 a partir de la rama actual.
3. Sube los cambias al respositorio remoto.
