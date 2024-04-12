# linktic-ecommerce
En este repositorio se subio solo uno de los servicios creados con Java que compone una aplicación web de tipo Ecommerce, con el fin de pasarlo por el flujo CICD en github actions

Debido a que durante la construcción del pipeline tuve un problema con la conexion de la base de datos del proyecto quiero dejar en este readme un comentario explicando el paso a paso de lo que hace el archivo .yml que me cree para construir el pipeline del flujo CICD en GithubActions, con el fin de darles a entender algo de mi conocimiento en la construcción de estos pipelines:

###################################################################
**name:** El nombre del flujo de trabajo, que en este caso es "Java CI".

**on:** Especifica los eventos que desencadenarán la ejecución del flujo de trabajo. En este caso, se ejecutará cada vez que se realice un push a la rama "main".

**jobs:** Define los trabajos que se ejecutarán como parte del flujo de trabajo. En este caso, solo hay un trabajo llamado "build".

**build:** Este trabajo se ejecuta en una máquina virtual Ubuntu y consta de varios pasos.

**services:* Define los servicios adicionales que se necesitan para ejecutar los pasos del trabajo. Aquí, estamos utilizando un servicio MySQL con la imagen de MySQL versión 8.0. Estamos configurando las credenciales de acceso y exponiendo el puerto 3606.

**steps:** Define los pasos individuales que se ejecutarán dentro del trabajo. Aquí, los pasos incluyen instalar Docker, realizar la configuración inicial del repositorio, configurar Java 17, esperar a que MySQL esté listo, compilar la aplicación con Maven, ejecutar las pruebas unitarias y ejecutar la aplicación Spring Boot.

