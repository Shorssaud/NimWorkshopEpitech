# Nim Language Workshop: Creating Conway's Game of Life

In this workshop, you will learn how to create a simple implementation of Conway's Game of Life using the Nim programming language. The Game of Life is a cellular automaton that simulates the evolution of a population of cells based on a set of rules.

FYI (for your information): ChatGpt sucks at nim, here is the nim documentation instead ;) 
https://nim-lang.org/docs/tut1.html

# Part 1

You will need Nim installed on your computer to continue

## Exercise 1: Setting up the Grid

In this exercise, create a file called game_of_life.nim. In it, create a grid of booleans of size 20x20 and print it

## Exercise 2: Parsing the Grid

In the same file, create a procedure which parses the entire grid, and another procedure which can count how many adjacent tiles (horizontal, vertical, or diagonal) are true

## Exercise 3: Implementing the Rules

In the same file, create a procedure which applies the following rules(in our case, live is true, dead is false):
Birth rule: An empty, or “dead,” cell with precisely three “live” neighbors (full cells) becomes live.
Death rule: A live cell with zero or one neighbors dies of isolation; a live cell with four or more neighbors dies of overcrowding.
Survival rule: A live cell with two or three neighbors remains alive.

## Exercise 4: Taking input

Finally, we will create a procedure which prints "Enter coordinates (x,y) to toggle cell state, 'r' to start, or 'q' to quit:" and takes input from stdin. These coordinates will then be used to create a live tile on the grid and start the game when the user has finished setting up a board

## Exercise 5: Basic Conway's game of life

Now, using all of the past procedures, we want to have a procedure which:
1. Asks the user for coordinates and filling in the grid until he is ready to start the game
2. With the pre-organized grid, printing out the grid every few seconds and updating it following the rules.

# Part 2

Amazing! You've managed to create Conway's game of life in Nim! However you may notice that the terminal is rather ugly and limiting, so lets make this visual using (lib here)

## Exercise 1:  ##
In this exercise, you will add obstacles to the game board. Obstacles will be represented by the character #. Copy the following code into game.nim:
https://github.com/nim-lang/nimble#installation
