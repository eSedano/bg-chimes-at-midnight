# Chimes at midnight
* Abstract strategy
* 2 players
* ?? minutes
## Introduction
In **Chimes at midnight**, two players compete to be the first one to capture the opponent's queen.
## Components

* 1 game board
* 10 pawns (5 white, 5 black)
* 2 queens (1 white, 1 black)
## Setup
Place the game board in between the players. Each player chooses the color to play with. Place each player's pieces following the configuration below. White plays first.

+----+----+----+----+----+
|    |    | bQ |    |    |
+----+----+----+----+----+
| bP | bP | bP | bP | bP |
+----+----+----+----+----+
|    |    |    |    |    |
+----+----+----+----+----+
| wP | wP | wP | wP | wP |
+----+----+----+----+----+
|    |    | wQ |    |    |
+----+----+----+----+----+

## Definitions

* **Reserve**: The stones close to a player, still not played on the board.
* **Buffer space**: Each of the 18 dark gray hexes on the board. Pieces can only be placed in buffer spaces when brough from the reserve or from another buffer space.
* **Regular space**: Each of the 37 white hexes on the board.

## How to play
### Actions
On their turn, players take one of the following actions:
* **Place a new stone**: Bring a stone from the reserve to an unoccupied buffer space.
* **Change buffer space**: Move one of their stones in a buffer space to another, unoccupied one.
* **Move a stone**: Move a stone from a buffer space or a regular space according to the stones' rules of movement.
* **Move a queen**: Move a queen on a regular space according to the queens' rules of movement.

A player may not perform a movement that leaves the board state unchanged.

### Rules of movement

#### Stones
Stones move in a straight line across the edges of the hexes, moving as far as possible. A stone's movement only stops when the next space is occupied by another piece or queen, or there are no more regular spaces to move to.

The following figure shows all possible moves for stone A, which would finish its movement in any of the spaces marked with an X.

<img src="stonemove1.png" alt="Move for stone 1" height="300"/>

The figure below shows all possible moves for stone A which, starting from a buffer space, could finish its movement in any of the spaces marked with an X.

<img src="stonemove2.png" alt="Move for stone 2" height="300"/>

### Queens

Queens also move in a straight line across the edges of the hexes. Unlike stones, queens are allowed to finish their movement on any regular space along the line of movement. The figure below shows all possible destination spaces for queen A marked with an X. 

<img src="queenmove.png" alt="Move for queen" height="300"/>

### Capture
A queen is captured when at least one of the following two conditions is met:
* Two stones (but not queens) of the opposed color surronds two of the queens' sides in a straight line (the queen is "sandwiched"). A queen moving in between two opponent pieces does not cause the queen to be caputed. Pieces surrounding a queen must be placed in regular spaces (i.e. pieces in buffer spaces are not taken into account when determining if a queen is captured) In the figure below, piece A moves and captures the black queen.

<img src="capture1.png" alt="Capture 1" height="300"/>

* A queen is left with no empty regular spaces surrounding it. In this case, it does not matter the color of the pieces surrounding the queen. In the following figure, both the white and the black queens are surrounded and captured.

<img src="capture2.png" alt="Capture 2" height="300"/>

When a queen is captured, the piece is flipped and returned to the owner's reserve as a **regular stone**.

## End of the game

The game ends when the two queens of one of the players are captured. The player with queens remaining on the board is the winner. If no queens remain on the board, the game ends in a tie.

## Possible changes based on feedback
The following items describe changes to the rules or the gameplay based on feedback received from testers. The changes are either \[F]ixes to the rules or \[V]ariants to the game:
* \[F] Clarify that captured queens are removed from the board and turned to regular stones in the reserve.
* \[V] Remove option to move pieces from one buffer space to another one.
