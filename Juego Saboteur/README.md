<!--Creado por Jonathan Carrero Aranda -->

**Saboteur** 🎮
==============
----------

This project consists of the development of a web portal that allows users to play online a board game called *Saboteur*. In this portal, a user will be able to create a user account 👤, create new games 🆕, join games already created by others 🤝 and, obviously, play in them 🕹️.

## Competencies and implementation 💻
---------------------------

Web page design using HTML and CSS, plus a web server implementation using *Node* and *Express.js*. Unlike the Planner, the use of *Bootstrap* is not allowed in the development of the game.

## Summary of the project structure by folder 📁
---------------------------

*   **controllers:** Files handling user requests to the server.
*   **Helpers:** Reusable methods for view generation, common across the project.
*   **integration:** Data Access Objects (DAOs) for database interactions (retrieving/inserting data).
*   **middlewares:** Core *Express.js* functions processing requests and responses.
*   **nbproject:** Internal files used by *NetBeans* IDE.
*   **public:** Publicly accessible files (index page, CSS, images, fonts, etc.).
*   **views:** `.ejs` files mixing data (model) with HTML (view) for game representation.

The rest of the files contain project metadata (`.json`), the database schema (`.sql`), or the application entry point (`app.js`).

## Basic user guide 📖
----------------------

In this game, each player takes the role of a dwarf searching for gold 💰 in a mine ⛏️. The mine is represented as a board with seven rows and seven columns.

<p align="center">
<img src="https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s1.png" alt="Game Board Start" style="border-radius: 15px;">
</p>

The players start from a starting square located in the middle row, first column. In the last column (rows 2, 4, and 6) there are three destination cells. Initially, the contents of these cells are unknown 🤔. The only thing the players know is that one of them contains a gold nugget ✨ and the other two contain nothing 🧱.

<p align="center">
<img src="https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s2.png" alt="Destination Cells" style="border-radius: 15px;">
</p>

There are two classes of players: **dwarf prospectors** and **dwarf saboteurs**. Each player is given a role (seeker or saboteur) at the beginning of the game, and this role remains secret 🤫 to the other players. Seekers and saboteurs have opposing objectives:

> *   **Seekers** aim to build tunnels along the board to reach the destination square containing the gold nugget.
> *   **Saboteurs** aim to block and divert the prospectors' tunnels so they *do not* get the gold nugget.

The game is played in turns. The player whose turn it is can do one of the following actions:

1.  **Place a path card on the board:**
    *   The tunnels on the new card must connect correctly with tunnels on adjacent, already placed cards.
    *   The new card must be reachable via a continuous path from the starting square.
    <p align="center">
    <img src="https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s3.png" alt="Placing a Path Card" style="border-radius: 15px;">
    </p>
    *   After placing a card, the player draws a new card from the deck 🃏.

2.  **Discard a card:**
    *   Each player starts with a hand of cards (the exact number depends on the player count, the description mentions 7 cards out of 15 possible types, which might need clarification - typically it's a hand limit and drawing from a larger deck).
    *   The player chooses a card from their hand to discard face-down.
    *   The player then draws a new card from the deck 🃏.
    <p align="center">
    <img src="https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s4.png" alt="Discarding a Card" style="border-radius: 15px;">
    </p>

3.  **Use an action card:**
    *   **Map (Magnifying glass 🔍):** Secretly look at one of the three destination cards.
    *   **Rockfall (Explosive 💥):** Remove a path card from the board (cannot remove start or destination cards).
    *   **Break Tool (Broken Pickaxe 🛠️):** Play on another player to prevent them from playing path cards.
    *   **Fix Tool (Fixed Pickaxe ✨):** Play on a player (including yourself) affected by a corresponding broken tool card to remove the restriction.
    <p align="center">
    <img src="https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s5.png" alt="Using Action Cards" style="border-radius: 15px;">
    </p>

All this is managed by a login system that allows users to consult at any time:
*   Games they are currently playing ⏳
*   Games that have been created and are available to join 🚪
*   Finished games (showing the result - win/loss) 🏆

<p align="center">
<img src="https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s6.png" alt="Game Lobby/Management" style="border-radius: 15px;">
</p>

At any time, a user can create their own game (and participate as a player).

<p align="center">
<img src="https://github.com/Joncarre/Programacion-web/blob/master/Juego%20Saboteur/images/s7.png" alt="Creating a New Game" style="border-radius: 15px;">
</p>

