# Practica GitPages Despliegue

![GitHub Logo](/images_gitPages/2.png)

Para poder entender mejor en que consiste este proyecto, hace falta explicar varios términos, como:

GIT, ¿Que es git y para que se utiliza?

GitHub es un sistema de gestión de proyectos y control de versiones de código, así como una plataforma de red social diseñada para desarrolladores. ¿Pero para qué se usa GitHub? Bueno, en general, permite trabajar en colaboración con otras personas de todo el mundo, planificar proyectos y realizar un seguimiento del trabajo.

Dentro de git, podemos encontrar la metodologia “git flow”. Esta metodologia simplifica el uso de git, y lo mejora de la siguiente manera:

Se crean 2 tipos de ramas:

Principales: Tiempo de vida infinito. No hace falta hacer commits sobre ellas, su funcion vendrá marcada por merges de otras ramas de funcionalidad.
	
	-Rama master: Siempre contiene un estado listo para la produccion 

	-Develop: Contine los ultimos cambios desarrollados para la proxima version de software. 	Cuando esta version es estable, esta rama se integra en master.

De funcion: Tiempo de vida finito(Feature, Release, Hotfix)

	-Feature: Cada nueva caracteristica de nuestro desarrollo debe residir en su propia rama 	feature. Usan develop como rama padre y cuando una caracteristica está completa se fusiona 	con develop.
	
	-Release: Una vez la rama de desarrollo haya adquirido suficientes caracteristicas para un 	lanzamiento (una fecha de lanzamiento está cerca) se crea una rama de version o release 	desde la rama develop.

	-Hot Fix: Se utilizan para reparar rapidamente las publicaciones de produccion en la que se 	han detectado errores. Es la unica rama que deberia bifurcarse directamente desde la master, 	y una vez que se ha arreglado los errores encontrados, se debe fusionar con las ramas master 	y develop



Desde nuestro equipo consideramos que esta metodologia es muy importante a la hora de desarrollar un proyecto porque tenemos todos los archivos perfectamente organizamos y se sabe en cada momento que es lo que hay que hacer, donde y como. También, se pueden prevenir errores criticos que de la forma convencional no se detectarian. 







USUARIO 1



El usuario 1 es el mas experimentado, y es el que se encargará de crear el repositorio del proyecto y de la estructura inicial de la pagina, donde incluirá la cabecera, la barra de lanevagcion con el acceso a home y el footer. En la parte central del home incluirá una breve descripcion del curso

![GitHub Logo](/images_gitPages/g_page.png)
![GitHub Logo](/images_gitPages/g_page2.png)

Después, adecua el proyecto a la metodología git flow.


git init
git flow init
git push -u origin master
git push origin develop

![GitHub Logo](/images_gitPages/eeeee.png)
![GitHub Logo](/images_gitPages/1.png)
![GitHub Logo](/images_gitPages/2.png)

Usuario 2

El usuario 2 crea 2 features, una para la sección “Modificar contenido HTML” con algún ejemplo, y otra para “Modificar atributos HTML”.


Primero nos situamos en la rama develop donde tenemos el contenido que ha subido el usuario 1

![GitHub Logo](/images_gitPages/11.png)

Y creamos los dos features, uno para cada implementación:

git flow feature start modificar_contenido_html

git flow feature start modificar_tributos_html

![GitHub Logo](/images_gitPages/112.png)

Nos situamos en la rama de modificar contenido html para el primer ejercicio con:

git checkout feature/modificar_contenido_html

Y procedemos al desarrollo del código




HTML:

![GitHub Logo](/images_gitPages/114.png)

JavaScript:

![GitHub Logo](/images_gitPages/115.png)

Como podemos ver, tenemos una etiqueta “p” con la id “demo”, que tiene el valor “JavasScript can change HTML content.”. Después, en el archivo .js asignamos a una variable el valor del botón en html, y seguido, le decimos que cuando haga click, el valor de la etiqueta “demo” será “Hello JavaScript”


Ahora nos situamos en la rama “modificar_atributos_html” como hemos hecho anteriormente con git checkout feature/modificar_atributos_html, y procedemos a la implementación del código como hemos hecho anteriormente. Una vez finalizado, procedemos a juntar las ramas que hemos creado con la rama develop.

Git add .
Git commit -m “feature_modificar_atributos_html”

git flow feature finish modificar_atributos_html


![GitHub Logo](/images_gitPages/116.png)

Lo mismo con la rama anterior “modificar_contenido_html”

![GitHub Logo](/images_gitPages/117.png)

Finalmente, hacemos el push de las nuevas implementaciones con

git push

![GitHub Logo](/images_gitPages/119.png)

Ahora, el usuario 3 implementará una feature de “modificar contenido css”, de igual manera que ha hecho el usuario 2, de la siguiente manera:

Primero, nos situamos en la carpeta del usuario 3 y cambiamos a la rama develop, y creamos la feature “modificar contenido css”

Clonamos el proyecto en la carpeta del usuario 3 con

git clone https://github.com/j-maestre/Practica_gitFlow

![GitHub Logo](/images_gitPages/118.png)

Hacemos git pull para actualizar el repositorio por si han habido nuevos cambios

![GitHub Logo](/images_gitPages/1192.png)

cambiamos a la rama develop

git checkout develop

Creamos una nueva feature llamada “modificar_contenido_css” como hemos hecho anteriormente y procedemos a la implementación del código:

git flow feature start modificar_contenido_css


Implementación del código:

HTML:

![GitHub Logo](/images_gitPages/css2.png)

JavaScript:

![GitHub Logo](/images_gitPages/css1.png)

Al igual que el usuario2, hemos creado una etiqueta “p” con la id “demo2”, con el valor “JavaScript can change the style of an HTML element”, y un elemento de tipo “boton”. Después, en el archivo js asignamos el valor del botón con id “mod_css” que hemos creado en el HTML, y le asignamos una función cuando hagamos click, que lo que hará será cambiar el estilo de esa etiqueta “p” con id “demo2”, y cambiará el tamaño de la fuente predeterminado a ‘35px’.






Una vez terminado el código, procedemos a la publicación de la feature nueva:


git add .
Git commit -m “feature_modificar_contenido_css”
git flow feature finish modificar_contenido_css

![GitHub Logo](/images_gitPages/git345345.png)

el usuario3 crea una release con todas las features etiquetándolas como v1.0

git flow release start v1.0
git flow release finish v1.0

![GitHub Logo](/images_gitPages/AA1.png)

git push

![GitHub Logo](/images_gitPages/AA3.png)

Por último, el usuario1 decide mejorar la sección creada por el usuario2, creando un hotfix “mejorasV_1_0” que efectua dicha mejora:

Primero vamos a la carpeta del usuario1 y hacemos git pull para actualizar el proyecto

Después, creamos un hotfix donde mejoraremos el código implementado por el usuario2

git flow hotfix start  mejorasV_1_0

![GitHub Logo](/images_gitPages/ZZZZ.png)

Una vez acabado el código, procedemos a la implementación del hot fix con:

git flow hotfix finish mejorasV_1_0

![GitHub Logo](/images_gitPages/ZZ.png)
