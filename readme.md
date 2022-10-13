This project create a tic tac toe game.

The first player using X and the second player using O. if the 3 same charaters in a line, then you won.


In the html file, we add 9 cells with the id of cellContainer, and a game status text and a restart button. Also add the link to css file and javascript file.

In the css file, we format the style of the cell.

For JS, which is the most important part of this project. Firstly we need to declare all of the variables we need. We select all cells. But for the status we do not select all, only select the text. followed by the restart button.
 
Winconditions will has two-dimensional array of indices, if three cells all have the same character we neet to check that, let's begin with the first row. These are the combinations of the winconditions.

For the let part.
We will need an array of placeholders I name this options.
This will be  the arrey of placeholders, an arrey of empty strings 9 of them, one for each cell.
we need to keep the track or current players.
we need to check if the game is runnning.we will switch this to true when we initialize our game.

Then let's create the functions we need to start.
function initializeGame
function cell clicked,updateCell,changePlayer,checkWinner and restartGame.



when we begin the game let's initialize the game. when start the game, running should be true. We'll use this function initialize game to take care of any setup before we need to start. we'll add some eventlisteners to our cells.
take our cells use for each method we will use an arrow function expression for each cell we will add our cell as eventlistner. we will add a callback of cellClicked then we will add an event listener to our restart button.
when we click we will evoke a restart function.
then we need to update the status text.

when we click a cell we will set a local varivale cellIndex, get a attribute which is cellIndex, 
I would like to check to see is if that index number within our options our placeholders are not empty. we only want to update a cell if there is nothing there.

if our options does not = emply space or the game is not running, then we will return :not do do anything.
otherwise will envoke the update cell function.


changeplayer:  If current player is X we will change to O otherwise, X.
And shows that it's X turn

for the checkWinner function. we will creat a temporary variable of roundwon, if somebody wins we will change this to be true.

Here we use a for loop, we will iterate all the win conditions within our two-dimensional array.
we will continue as long as the we get the result.

begin with the first array.
Each row has three indices.
if cell A is emply space or cell B is emply space or cell C is empty space 
if cell A = cellB and cellB =cellC for example, if the first 3 cells are not empty spaces 
and they are all the same characters that means somebody won. if there is no winner we will check the next set of win conditions.
if all of them are empty space we will continue to do that.
if they are the same charaters, then evoke rounwon. which means we have winner and can break the loop.

if roundwon is true we need to change the status text here = currentplayer wins
running = flase the game is over.
else if our options does not include any empty spaces. if this is true
them we will update our status text with draw.



For restart button.just empty all the cells, and shows 's currentplayer's turn. We use each cell functions to update the text content to empty space, running =true. 
we have a new game.