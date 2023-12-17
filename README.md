Interactive Sequence Memory Game with 5 levels using numbers and letters, that would challenge users to physically interact with the board. Using the button on the DE10 Lite board to start the game, the LEDR’s to display the sequence that needs to be repeated, use the switches to mimic the shown sequence in the exact same order and lastly the use of a second button to indicate that the player has finished the sequence. There will also be a time limit for each level that will decrease each time a higher level is achieved. All 9 LEDR’s will be used and as the levels progress, the generated sequence will become harder to mimic due to a rapid clock time.


Combinational Logic: Used for sequence evaluation to compare the player’s input to the sequence stored in the register by comparing bits. Aswell, as controlling the LEDR displays to ensure that the lights are showing up at the correct corresponding LEDs and game initialization with the buttons to ensure positions are triggered.

Sequential Logic: Used for sequence memory where registers can be used to store each level sequence for the player to memorize. Also, used for scorekeeping to keep track of the player’s progress and determine whether the player gets to advance to the next level or continue playing their current level (using ‘posedge’). Lastly, it will be used for game management - to detect whether a sequence has been completed, if the game runs when the button is pressed and displaying whether the player’s input is correct or incorrect.

