<!--Creado por Jonathan Carrero Aranda -->

**Saboteur**
==============
----------

This project consists of the development of a web portal that allows users to play online a board game called *Saboteur*. In this portal, a user will be able to create a user account, create new games, join games already created by others and, obviously, play in them.

## Competencies and implementation
---------------------------

Web page design using HTML and CSS, plus a web server implementation using *Node* and *Express.js*. Unlike the Planner, the use of *Bootstrap* is not allowed in the development of the game.

## Summary of the project structure by folder
---------------------------

**controllers:** are the files where the collection of requests made by the user to the server as he/she interacts with the application is carried out.

**Helpers:** set of methods that help to form the view and that, mostly, are common to a great part of the project.

**integration:** Data Access Objects that retrieve and insert information to the database are stored here (as they are in the integration layer).

**middlewares:** is the division on which *Express.js* is based. A middleware is a function that receives a *request* object with the user's request data and a *response* object with the response accumulated so far. During execution, a middleware can read/modify both objects.

**nbproject:** internal files used by *NetBeans* (IDE used for application development).

**public:** here are the public files of the project, that is to say, those necessary resources that are directly exposed to the client. Some of the files contained are: the *index* page, fonts, the CSS of the application, images used, etc.

**views:** are the .ejs files, which will mix the model (data) with the view (HTML) to be properly represented when we are playing.

The rest of the files contain information about the project (.json), the database used (.sql) or the entry point in the application execution flow (app.js).

## Basic user guide
----------------------

In this game each player takes the role of a dwarf searching for gold in a mine. The mine is represented as a board with seven rows and seven columns. 

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s1.png)

The players start from a starting square which is located in the cell located in the middle row, first column. In the last column (rows 2a, 4a and 6a) there are three destination cells. Initially the contents of these cells are unknown. The only thing the players know is that one of them contains a gold nugget and the other two contain nothing.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s2.png)

There are two classes of players: dwarf prospectors and dwarf saboteurs. Each player is given a role (seeker or saboteur) at the beginning of the game, and this role remains secret to the other players. Seekers and saboteurs have opposing objectives: 

- Seekers aim to build grottoes along the board in order to reach the destination square containing the gold nugget.
- The saboteurs have the objective of blocking and diverting the dwarf prospectors' caves so that they do not get the gold nugget.

The game is played in turns. The player whose turn it is can do one of the following actions:

- Place one of his cards on the board: to place one of his cards on the board it must be fulfilled (a) the grottoes of the new card fit with some of the grottoes already placed and (b) the new card must be reachable from the starting square.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s3.png)

After having placed a card, the player will receive a new randomly generated card.

- Discard one of his/her cards: Each player is dealt a total of 7 cards out of the 15 possible cards he/she can play. The player will discard one of his/her cards (the one he/she wishes), and will then receive another randomly generated card.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s4.png)

- Use a special card between magnifying glass (look at a square on the board), explosive (break a grotto card), break tool (block a player) or fix tool (unblock a player).

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s5.png)

All this is managed by a login system that allows users to consult at any time the games they are playing, the games that have been created and that they can join and the games already finished (with the result if they won or not).

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s6.png)

At any time, a user could create his own game (in which he would participate as if he were another player).

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s7.png)

