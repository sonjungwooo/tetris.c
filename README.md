# tetris.c
> 단국대학교부속소프트웨어고등학교 포트폴리오

## Development Motivation
Having experienced both success and failure, I resolved to create my own game using C. This determination led me to start developing a Tetris game.

## Development Languages and Tools
After initially creating a shooting game with Pygame, I became inspired to build a more refined version of Tetris using advanced features of the C language. I developed this project using Visual Studio Code, which is the tool I use most frequently.

## Development Process
First, I played various Tetris games made by others. Then, I implemented the shapes used in the game by applying their coordinates within a structure array called shape in my Tetris. Additionally, I utilized a function named nFrame to adjust the falling speed of the shapes, and I implemented a switch-case statement to allow the arrow keys to change the position of the shapes.

## Description
DrawScreen: Draws the entire screen, including the game board, game title, and even the walls, all at once.

DrawBoard: Draws only the game board. In other words, it renders only the stacked bricks on the board, excluding external walls and other text.

ProcessKey: Handles key input. This function is separated from the main function to lighten its load, and it returns TRUE when the moving brick touches the bottom.

PrintBrick: Displays or deletes a brick. Since it targets the brick that is in motion, it references the global variables brick, rot, nx, and ny.

GetAround: Checks what is present around a brick to determine the possibilities for movement and rotation. Instead of inspecting the surroundings of the moving brick, it observes the shape of the brick based on the provided position.

MoveDown: Moves the brick down by one row. If it reaches the bottom, it calls the TestFull function and returns TRUE.

TestFull: Identifies any row that is completely filled horizontally and deletes it.

## Reflection and Overcoming Challenges
The most challenging aspect of completing the Tetris game was making a filled line disappear. This was difficult because, after confirming that a row was completely filled, it had to be removed and the rows above it needed to drop down. Overcoming this challenge took considerable time and required me to think through many approaches and try various methods. My goal is to be admitted to Dankook University Affiliated Software High School, and I plan to further learn and master game engine usage to create more impressive graphics and develop games that many people can enjoy.
