<!--Creado por Jonathan Carrero Aranda -->

**Planificador de cursos**
==============
----------
     
En este pequeño proyecto se implementa una aplicación web muy básica para gestionar cursos presenciales de diversa índole: programación, cocina, baile, música, etc. El servidor contendrá una base de datos con cursos disponibles. Los usuarios de la aplicación pueden buscar un determinado curso a partir de su nombre y registrarse en uno o varios cursos.

## Competencias e implementación
---------------------------

El objetivo principal es la implementación de APIs tipo REST y el desarrollo de una aplicación web utilizando AJAX y el modelo SPA.
Una aplicación SPA (*Single Page Application*) es una aplicación web cbontenida en un úncio documento HTML. Los componentes de este documento de muestran u ocultan a medida que el usuario interactúa con la aplicación web.

También se hace hincapié en el correcto diseño de la API RESTful y su implementación en *Express.js*. Por otro lado, el servidor funciona a través del protocolo HTTPS.

Se ha hecho uso de tecnologías como Bootstrap para facilitar el posicionamiento de los elementos y de bases de datos relacionales con *MySQL* gestinado a través de *PhpMyAdmin*.

## Resumen de la estructura del proyecto por carpetas
---------------------------

**helpers:** conjunto de métodos que ayudan a formar la vista y que, mayoritariamente, son comunes a gran parte del proyecto.

**integration:** aquí se almacenan los Data Access Object que recuperan e insertan información a la base de datos (pues se encuentran en la capa de integración).

**nbproject:** ficheros internos que usa *NetBeans* (IDE utilizado para el desarrollo de la aplicación).

**node_modules:** módulos utilizados por *Node* (lado del servidor).

**public:** aquí se encuentran los ficheros públicos del proyecto, es decir, aquellos recursos necesarios que son directamente expuestos ante el cliente. Algunos ficheros contenidos son: la página *index*, bibliotecas como jQuery, el CSS de la aplicación, imágenes usadas, etc.

**routes:** contenedor de los routers. Un route es como una mini-aplicación web con sus propias rutas y su propia cadena de middlewares. En este caso, tan sólo tenemos dos router: users y cursos.

El resto de ficheros contienen información acerca del proyecto (.json), la base de datos utilizada (.sql), la certificación para el uso del protocolo HTTPS o el punto de entrada en el flujo de ejecución de la aplicación (app.js).

## Guía básica de uso
---------------------------

Al entar en el planificador ya podemos consultar los cursos disponibles sin necesidad de estar registrados. Ahora bien, si lo que queremos es tener una buena organización y poder inscribirnos en los cursos, entonces sí es necesario tener una cuenta.

Cuando hacemos la búsqueda de cursos, dicha búsqueda realiza una comprobación en la base de datos y muestra todos los cursos que contengan, en su título, la cadena buscada. Si por ejemplo buscamos *cocina*, apareceran todos los resultados que contengan esa palabra.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen1.png)

Si pinchamos sobre un curso podemos ver información acerca del mismo, pero como es lógico, no nos dejará inscribirnos hasta que no estemos registrados.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen2.png)

Una vez registrados, podemos empezar a crear cursos que puedan interesar a otro usuarios de la aplicación. Además, el sistema organiza los cursos de tal forma que sea fácil para el usuario consultar los cursos que ya ha terminado, los que está cursando actualmente y qué horario tiene establecido para cada semana.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen3.png)
