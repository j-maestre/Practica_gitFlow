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
