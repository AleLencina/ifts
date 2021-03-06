# farma-soft
Aplicación Web en Flask creada para exámen parcial de Paradigmas de la Programación (IFTS N°18)

------------------- F A R M A - S O F T ---------------


--------------------- Introducción ---------------------

- La Aplicación Farma-Soft fue creada para satisfacer las necesidades de búsqueda en una extensa base de datos en donde se registran ventas realizadas en el rubro de farmacia. Fue integramente desarrollada en el lenguaje de programación Python3

------------------------ Módulos -----------------------

- Se han utilizado diversos módulos y frameworks:

- csv
- flask
- flask_moment
- flask_script
- flask_wtf (formularios)
- flask bootstrap

--------------------- Flujo del programa ---------------

- Para poder ejecutar el programa debemos abrir un terminal de linux y tener instalado Python3, con el paquete pip, el cual servirá para instalar todo lo necesario(virtualenv, flask y bootstrap). Fue creado un entorno virtual para el desarrollo, llamado flaskEnvironment.

- El archivo principal, app.py, será la guía mediante la cuál se ejecutarán todos los procesos, ya que de ser necesario acudirá a otros módulos, clases, funciones, bases de datos e incluso nos mostrará en un navegador un sitio web, que será la interfaz mediante la cual el usuario se comunicará con la base de datos, y a su vez recibirá respuestas de la misma.

- Comienza a ejecutarse desde los "imports", siguiendo por el primer test al cual es sometida la base de datos "farmacia.csv", luego nos mostrará, a través del puerto del servidor local 127.0.0.1:5000 la primer pantalla, donde se invitará al usuario a acceder a la aplicación a través del primer menú.

- Una vez ingresado, podrá interactuar con las opciones de búsqueda.

--------- Datos, procesos, estructura de los mismos e interfaz--------

- La estructura se pensó intentando, desde un primer momento, separar las Vistas del Modelo y los Controladores (buscar modelo MVC para más información). Por lo tanto, tendremos las bases de datos o bien "modelos" (farmacia.csv, donde se registran las ventas y usuarios.csv, donde están los nombres de usuario con sus contraseñas). Las "Vistas", que están en la carpeta "templates", las cuales son documentos HTML que hacen de "canal" para mostrar los datos obtenidos de las bases de datos. Son la cara visible de la aplicación. Estos archivos se desarrollan a partir de 2 templates principales: ingreso_base.html e index_base.html. Y por último, tendremos los controladores, que conducen a la aplicación hacia el funcionamiento y la comunicación con el usuario. El principal, como antes mencionamos, es app.py, que es centro que unifica a todos los procesos, tales como:

- preparaCsv.py: Este archivo busca en la base de datos los campos, los organiza y los deja preparados para su consulta rápida. Consta de la creación de una clase llamada Csv.

- formulariosFlask: Usa unas pocas líneas de código para realizar unos formularios web con validación incluída. Los mismos son llamados desde app.py para que formen parte de los html cuando es el momento de pedir datos al usuario.

- busqueda.py: Este proceso tiene preparadas unas funciones que se encargan de hacer la selección lógica de la información a mostrar, de acuerdo con lo solicitado por el usuario. A través de este proceso, también es posible escribir en el archivo "usuarios.csv", en caso de que tengamos a un usuario nuevo frente a la aplicación.

---------------------- Porqué creamos clases? ---------------------------

La creación de clases hacen que la aplicación pueda tener una estructura más genérica, que es según nuestro punto de vista algo muy importante, ya que el código puede ser reutilizado. Pero además, la programación orientada a objetos, permite ahorrar líneas de código y hacer más fácil de entender lo realizado.
 
 Las clases creadas fueron: 

1 - Las que corresponden a los formularios wtf. LoginForm, ProductForm, ClienteForm y CrearUsuario son los cuatro diferentes y posibles formularios. Estas clases heredan todas las características de una principal que se importa de flask, llamada FlaskForm().

2 - Las de preparaCsv: la clase Csv ordena los campos obtenidos de la bas de datos y los devuelve en mayúscula.

3 - validacion.py tiene dos clases creadas, mediante las cuales se intenta captar algún posible error y manejarlo de manera tal que no detenga el flujo.





# ifts
