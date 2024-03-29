# CPSC481-project
# How to run the Minotaur AI Maze

1.) If you do not have pygame and Pillow installed already, use the commands:
    ```
    pip3 install pygame
    ```
    and
    ```
    pip3 install Pillow
    ```
       
2.) Download the zip file that has all of the necessary files.   

3.) Select the main2.py to run the program using the command:
```
python3 main2.py
```
Then use the arrow keys to control the player. 

Try to pick up the key, then head to the stairs to win.

Then go back to the console and type 'Y' to generate a new maze.

Then the program will continue this cycle until you lose, or hit 'n' to stop playing the game.

# FILE DESCRIPTIONS
Dungeon.py
       - This file generates the game's maze/dungeon. The class Generator() includes numerous features of the maze such as the maze's width, height, tiles, and the rooms within the maze/dungeon. Generator() includes several functions that essentially updates the dungeon when a move from either the player or AI has occurred. Furthermore, these functions generate the 4 rooms within the dungeon, generate corridors/hallways that connect rooms, generate the Minotaur enemies, and renders the images used for the Minotaur and Player characters as well as the surrounding walls and cells for the maze/dungeon. 
       
main2.py
       - This is the main driver for the program. The main GUI window is implemented here along with the game loop. A dungeon is first created before the program enters the game loop. then on subsequent plays, new dungeons and random placement of enemies are generated.
       
maze.py
       - This file generates the OLD maze generation in the dungeon. This file also generates the cells and its surrounding walls within the maze. Each cell may be surrounded by north, east, south, or west walls. We utilized Christian Hill's 2017 depth-first algorithm ( https://scipython.com/blog/making-a-maze/ ) to help us generate the maze. Essentially, the program starts at a specific coordinate and creates a random structure for the maze, finding cell neighbors and establishing where to knock down the wall to create a path. However, this version of the code does not scale with the screen, creating weird visuals. This should not be run, as it it not he final culmination of the project. 
       
Minotaur.py
       - This file generates the Minotaur character and its behavior. The functions included in the file are the critical algorithms and formulas that drive the Minotaur. Such algorithms and formulas include the distance formula, best first search, and depth first search algorithms. 
       
Player.py
       - This file generates the player character. The function render() sets different images/views of the player for every direction it is facing. The function move() receives the user's desired direction and utilizes key listeners to move in the specified direction. Additionally, the player's position updates as the player selects the different directions.
       
Resources
       - The resources folder contains all .png files needed to render the program with its user and AI. Various .png files are used to represent each movement the user performs as well.
