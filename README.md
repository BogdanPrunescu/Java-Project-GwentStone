# Tema POO  - GwentStone

<div align="center"><img src="https://tenor.com/view/witcher3-gif-9340436.gif" width="500px"></div>

## Homework Structure

The homework uses two main classes to execute and run the games:

**AppManager** -> The class that prepares each test by taking all the players’ decks and all the matches.

**GameManager** -> The class that prepares each game and runs the actions given in the input. 
GameManager also handles storing the elements of a game: the cards on the table, the cards in 
the players’ hands, the heroes, the player whose turn it is at a given moment, the hand that 
must be dealt to each player, etc.

In addition, I created other classes to modularize output printing and the handling of invalid cases:

**DebugCommands** -> Has a single static function where I handle the debug commands. For some cases,
I had to clone the output because I needed a copy of the reference in order to display the status
of an object at a given moment.

**Conditions** -> A class that contains test functions for certain game conditions, such as checking 
whether a player has a tank, whether the HeartHound card can be used, etc.

**PrintOutput** -> A helper class that I use to print outputs fairly easily. It has many constructors,
which are used depending on what I want to display in the output.

**PrintErrors** -> Contains functions that are called when invalid cases occur.

The Card class contains universal information for every class that inherits from it. The Minion, 
Environment, and Hero classes inherit from the Card class, and each of them contains functions 
for running the input commands specific to them. For example, the Minion class implements the 
placeCard, attack, and useAbility functions.

Below, I attached an image where all the classes related to the game cards can be seen.

<div align="center"><img src="img/package.png" width="500px"></div>


