# lightsout
Good luck! There should be at least one winning combination
I used class based components for this project. Top level App component, 
and beneath that is the stateful Board component, where the majority of the game logic lies.
Finally, there is a simple render component which I called "Cell" that simply displays each 
cell based on the state from above. I passed the state("isLit") of each tile down as props in the render method, along with 
a method that was also passed as props, "flipCellsAroundMe. When the method is called onClick,
a function called "flipCellsAround" is invoked in the <Board /> component, where the x and y coordinates are passed through as "coord". From there,
some simple logic just flips each of the neighboriding tiles (above,below,left,right) and that tile itself. The game is over when all tiles have a state of 
isLit: false.
At that point some logic runs to check if all tiles are (isLit: false), and if thats the case, the state for hasWon will flip to be true!
