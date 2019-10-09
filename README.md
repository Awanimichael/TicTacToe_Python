# TicTacToe Game
TicTac to is a board game played by two players. 

## The following are Implemented
* [X] Do we have a winner?
* [X] At every state of the board, is the next move a player is proposing to make valid?

## Assumptions that are made in this solution
* [X] There is one board
* [X] The board will always consist of 3x3 cells
* [X] The game is played between a human player Vs computer player
* [X] Human will be the first player
* [X] cells can either be "empty", "X" or "O"
* [X] "X" represents human player and "O" represents computer
* [X] The game automatically alternates between human and computer

## Game Design
I have created a class **BoardGame** This class has several methods
* **display()** - displays the board as a list of 3x3 cells
* **makeMove()** - computer makes a ramdom move from the list of available cells on board
* **humanMove()** - Promt player to select a cell by choosing from alphabets A - I representing each cell in the 3x3 board. It checks if it is a valid move (cell within board range and not already picked)
* **humanBoardUpdate()** - Updates the board with human picked cell
* **computerBoardUpdate()** - calls the makeMove method to generate a random number within range and updates board.
* i**sThereAWinner()** - creates a list of winning moves. and checks board if the list exist return True otherwise false

I have also implemented a ``**playGame()**`` function outside the class
* It creates an object (**ticTacToe**) of the class (**BoardGame**)
* Simulates the process of playing the game, by alternating between human and computer

### How TicTocToe is Played
Game starts by calling the **playGame(**) function
* The playGame instantiate the class, and displayed an empty board.
* Then it prompts the human to make a play, by calling humanMove() method which checks if its a valid move 
* If valid, updates the board accordinly. Otherwise display an Invalid message and prompt another respose 
* It checks of its the winner after every move. If there isnt a winner yet, then computer makes a move.
* Computer calls the makeMove() method. which will always make a valid move. Filtered empty spaces in board
* It also checks if its a winner after every move. If there is no winner yet, its alternates back to player.
* If end of list is reached. It means the game is a tie. There is no winner
* Game ends.


### Strategies that can be used to test the program
I have implemented testing this program by creating a playGame() method that simulates the play. 
Other testing methods include.
* Unit testing and fuctional testing
* Testing each unit with test cases to ensure that is gives desired output.
* For example we can test to see if a move is valid by calling the humanMove() with test parameters
```python

print(humanMove(["X","O","X","O","X","O","X","O"])) 

```
this will promt the user to pick a cell value and will return and Invalid Error, because all cells are picked.
* Other test cases could be entering a number not in the board, or entering a negative number.


