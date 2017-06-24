<!--Creado por Jonathan Carrero Aranda -->

**Saboteur**
==============
----------

Este proyecto consiste en el desarrollo de un portal web que permita a los usuarios jugar en línea a un juego de mesa llamado *Saboteur*. En este portal, un usuario/a podrá crear una cuenta de usuario, crear nuevas partidas, unirse a partidas ya creadas por otros y, obviamente, jugar en ellas.

## Competencias e implementación
---------------------------

Diseño de páginas web mediante HTML y CSS, además de una implementación en el servidor web utilizando *Node* y *Express.js*.
Al contrario que en el Planificador, no está permitido el uso de *Bootstrap* en el desarollo del juego.

## Resumen de la estructura del proyecto por carpetas
---------------------------

**controllers:** son los ficheros donde se lleva a cabo la recogida de peticiones que va realizando el usuario al servidor a medida que interactúa con la aplicación.

**helpers:** conjunto de métodos que ayudan a formar la vista y que, mayoritariamente, son comunes a gran parte del proyecto.

**integration:** aquí se almacenan los Data Access Object que recuperan e insertan información a la base de datos (pues se encuentran en la capa de integración).

**middlewares:** es la división en la que se basa *Express.js*. Un middleware es una función que recibe un objeto *request* con los datos de la petición del usuario y un objeto *response* con la respuesta acumulada hasta el momento. Durante la ejecución, un middleware puede leer/modificar ambos objetos.

**nbproject:** ficheros internos que usa *NetBeans* (IDE utilizado para el desarrollo de la aplicación).

**public:** aquí se encuentran los ficheros públicos del proyecto, es decir, aquellos recursos necesarios que son directamente expuestos ante el cliente. Algunos ficheros contenidos son: la página *index*, fuentes, el CSS de la aplicación, imágenes usadas, etc.

**views:** son los ficheros .ejs, los cuales mezclarán el modelo (datos) con la vista (HTML) para ser representados adecuadamente cuando estemos jugando.

El resto de ficheros contienen información acerca del proyecto (.json), la base de datos utilizada (.sql) o el punto de entrada en el flujo de ejecución de la aplicación (app.js).

## Guía básica de uso
---------------------------

En este juego cada jugador toma el papel de un enano que busca oro en una mina. La mina se representa como un tablero de siete filas y siete columnas. 

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s1.png)

Los jugadores parten de una casilla de salida que se encuentra en la celda situada en la fila central, primera columna. En la última columna (filas 2a, 4a y 6a) existen tres casillas de destino. Inicialmente el contenido de esas casillas es desconocido. Lo único que los jugadores conocen es que una de ellas contiene una pepita de oro y las dos restantes no contienen nada.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s2.png)

Existen dos clases de jugadores: enanos buscadores y enanos saboteadores. Cada jugador recibe un rol (buscador o saboteador) al principio de la partida, y este rol permanece secreto para los demás jugadores. Los buscadores y los saboteadores tienen objetivos contrapuestos: 

- Los buscadores tienen como objetivo construir grutas a lo largo del tablero con el fin de llegar a la casilla de destino que contenga la pepita de oro.
- Los saboteadores tienen como objetivo bloquear y desviar las grutas de los enanos buscadores con el fin de que éstos no consigan la pepita de oro.

El juego transcurre por turnos. El jugador que tiene el turno puede realizar una de las siguientes acciones:

- Colocar una de sus cartas en el tablero: para colocar una de sus cartas en el tablero debe cumplirse (a) las grutas de la carta nueva encajan con algunas de las grutas que ya hay puestas y (b) la carta nueva debe ser alcanzable desde la casilla de salida.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s3.png)

Tras haber colocado una carta, el jugador recibirá una carta nueva generada aleatoriamente.

- Desechar una de sus cartas: A cada jugador/a se le reparte un total de 7 cartas de entre las 15 posibles que pueden tocarle. El jugador eliminará una de sus cartas (la que él/ella desee), recibiendo a continuación otra carta generada aleatoriamente.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s4.png)

- Utilizar una carta especial entre lupa (mira una casilla del tablero), explosivo (rompe una carta de gruta), romper herramienta (bloquear a un jugador) o arreglar herramienta (desbloquear a un jugador).

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s5.png)

Todo esto es gestionado por un sistema de login que permite a los usuarios consultar en todo momento las partidas en las que están jugando, las partidas que se han creado y a las que pueden unirse y las partidas ya terminadas (con el resultado si ganaron o no dichas partidas).

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s6.png)

En cualquier momento, un usuario podría crear su propia partida (en la que participaría como si fuese un jugador más).

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s7.png)

