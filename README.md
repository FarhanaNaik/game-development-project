
# Project Title

Minesweeper is a puzzle game generally played on personal computers. The game features a grid of clickable squares, with hidden "mines" scattered throughout the board. 
The objective is to clear the board without detonating any mines, with help from clues about the number of neighboring mines in each field.

Rules:-

   Minesweeper rules are very simple. The board is divided into cells, with mines randomly distributed. To win, you need to open all the cells. The number on a cell shows
   the number of mines adjacent to it. Using this information, you can determine cells that are safe, and cells that contain mines. Cells suspected of being mines can be 
   marked with a character(p) using the right mouse button.


## Front End
HTML - A markup language for describing web documents.
CSS - A style sheet language used for describing the look and formatting of a document written in a markup language.
Java Script - A programming language of the Web.
## Installation
can install from here https://code.visualstudio.com/
## HTML & CSS:-

<!DOCTYPE html>
<html>
	<head>
	
		<title>mendel's minesweeper</title>
	    
		<script src="mine.js"></script>
		<style>
			.container{
    background: aquamarine;
    margin-left: 50px;
    margin-right: 120px;
   

}
		</style>
		
	</head>
	<body>
		<div class="container">
		
			<h2 style="color: blue;">MineSweeper</h2>
	<center><canvas id="game" width="300" height="400">
	</canvas></center>
	</div>
	</body>
</html>
## Javascript
When developing this game, there are two key areas. The first is how the grid itself is built:

[grid] = [array of tiles, width x height]

[placed mines] = 0

do until [placed mines] == [desired number of mines]:
	[pos] = select random tile
	
	if [pos] has mine then restart 'do' loop
	else:
		[grid][pos] has mine
		[placed mines] + 1
(loop)

foreach [pos] in [grid]:
	set [grid][pos] danger = (number of adjacent tiles that have mines)
(loop)
User interaction
Once our grid has been built, we handle user input. This consists of the user clicking on a tile, as well as a function that handles revealing the tile to the player, and works as follows:

function reveal tile ( [tile] ):
	set [tile] revealed
	
	if [tile][danger] == 0:
		foreach [n] in [neighbours]:
			reveal tile( [n] )
		(loop)
end function

if [clicked tile] has mine: game over
else:
	reveal tile( [clicked tile] )
	
	if [all tiles without mines] are revealed:
		game won
## Links

Initial view:-
http://127.0.0.1:5501/index.html

it consists of three levels:-
Easy::-http://127.0.0.1:5501/index.html
Intermediate ::-http://127.0.0.1:5501/index.html
Hard::-http://127.0.0.1:5501/index.html

-->Setting the font we wish to use, we then show the frame rate in the top-left corner of the Canvas

--->When a new level is started with the startLevel method, it is passed the difficulty level which will be played (diff), and begins by resetting the gameState newBest and timeTaken properties, changing the screen to playing, and the difficulty to the provided diff. We also set the gameTime and lastFrameTime to 0 and empty the grid array.








## conclusion

concepts are covered 
->Global variables and objects
->Grid Tile objects
->Game State and starting a new level
->Updating game logic
->window onload 
->Drawing menu
->Drawing the game playing win or lost
->Main Game Loop