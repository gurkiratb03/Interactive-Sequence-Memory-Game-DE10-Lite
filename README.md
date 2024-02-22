# Interactive Sequence Memory Game 

## Project Description

The Interactive Sequence Memory Game is a captivating project designed for the FPGA-based DE10 Lite board, challenging participants to remember and replicate a series of numbers and letters. This endeavor spans five increasingly difficult levels, harnessing the FPGA's bespoke real-time processing capabilities for a compelling, real-time interactive experience. The game ingeniously utilizes the FPGA’s ability to efficiently process complex logic, enabling a lively and immersive gameplay experience. Players engage with the game by using the board's buttons, LEDR displays, and switches, sharpening their memory and concentration skills. The game not only provides entertainment but also demonstrates the adaptability and strength of FPGA technology for interactive digital designs. Gameplay involves initiating the challenge with a button press, observing the LEDR-displayed sequence, and then accurately reconstructing it using the board's switches. A second button confirms the completion of the sequence. To intensify the challenge, each advancing level shortens the available time to complete the sequence, and the clock speed increases, making the sequences more difficult to follow. All nine LEDRs are utilized, ensuring a comprehensive and escalating test of the player’s memory as they progress through the game’s stages.

## Functionality 

## Hardware

* DE10 Lite board

## Combinational and Sequential Logic

* Combinational Logic: Used for sequence evaluation to compare the player’s input to the sequence stored in the register by comparing bits. Aswell, as controlling the LEDR displays to ensure that the lights are showing up at the correct corresponding LEDs and game initialization with the buttons to ensure positions are triggered.
* Sequential Logic: Used for sequence memory where registers can be used to store each level sequence for the player to memorize. Also, used for scorekeeping to keep track of the player’s progress and determine whether the player gets to advance to the next level or continue playing their current level (using ‘posedge’). Lastly, it will be used for game management - to detect whether a sequence has been completed, if the game runs when the button is pressed and displaying whether the player’s input is correct or incorrect.

## Testable Features

## Combinational Logic

- `Input-Output Correspondence`: Ensures that the appropriate LEDR responds to each switch input.
- `Real-Time Response`: The game provides immediate acknowledgment of right or wrong sequence entries.
- `Immediate Error Signaling`: Instantly flags any input that doesn't match the expected sequence.

## Sequential Logic

- `Sequence Storage Verification`: Maintains the integrity of sequence memory throughout the game.
- `Smooth Stage Navigation`: Ensures seamless transitions from one level to the next.
- `Precise Timing Control`: Maintains strict timing for sequence display and player input recognition.
- `Score Tracking`: Keeps an accurate tally of the player's score following the completion of each stage.

## How to Play

1. Game Activation: Press the designated button on the DE10 Lite board to start the game, which opens with an introductory display on the LEDRs.
2. Sequence Observation: Focus on the LEDR display as it presents a sequence of numbers and letters, which grows more intricate at each stage.
3. Sequence Imitation: Utilize the DE10 Lite board's switches to duplicate the sequence displayed by the LEDRs, with each switch corresponding to a particular element in the sequence.
4. Answer Confirmation: Once you have entered the sequence, hit the second button to confirm your input.
5. Level Progression: Succeed in replicating the sequence correctly to progress to the subsequent level, as the game monitors your success and escalates the challenge.


## Files Description

* `ClockDividerFAST.v` & `ClockDividerSLOW.v`: Modules for controlling the timing of sequences displayed to the player.
* `DE10_LITE_Golden_Top.v`: The top module that integrates all components of the game.
* `display.v` & `displayLetters.v`: Modules responsible for displaying numbers and letters on the LEDR's.
* `lfsr10bit.v`: A module for generating random sequences using a linear-feedback shift register.
* `project.v`: The main project file that combines all functionalities of the Sequence Memory Game.
