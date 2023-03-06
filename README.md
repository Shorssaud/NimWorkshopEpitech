# Nim Language Workshop for Game Development #
Welcome to the Nim Language Workshop for Game Development! In this workshop, you will learn the basics of the Nim programming language and use that knowledge to create a simple game.

## Introduction ##
Nim is a systems programming language with a focus on safety, efficiency, and expressiveness. It is designed to be easy to read and write, and it compiles to C, C++, or JavaScript. Nim is strongly typed and supports features such as generics, metaprogramming, and garbage collection.

## Exercise 1: Setting up the Game ##
In this exercise, you will set up the basic structure of the game. Create a new file called game.nim and copy the following code into it:

```
import strutils

var player_position = 0
const game_board = "S*--*--*--*--*--*--*--*F"

proc print_board() =
  echo game_board
  var marker = " " * player_position & "^"
  echo marker

print_board()
```

Save the file and run the following command in your terminal:

```nim c -r game.nim```

This will compile and run the program, and you should see the game board and the player marker.

## Exercise 2: Moving the Player ##
In this exercise, you will add code to allow the player to move left or right on the game board. Copy the following code into game.nim:

```
proc move_player(direction: string) =
  var new_position = player_position
  if direction == "left" and player_position > 0:
    new_position -= 1
  elif direction == "right" and player_position < len(game_board) - 2:
    new_position += 1
  player_position = new_position
  print_board()

while true:
  var input = readLine(stdin)
  if input == "q":
    break
  elif input == "left":
    move_player("left")
  elif input == "right":
    move_player("right")
```
Save the file and run the command nim c -r game.nim again. This will compile and run the game. You should be able to move the player left or right on the game board by typing "left" or "right" and hitting enter.

## Exercise 3: Adding Obstacles ##
In this exercise, you will add obstacles to the game board. Obstacles will be represented by the character #. Copy the following code into game.nim:

```
import random

const obstacle_chance = 0.2

proc generate_obstacle() =
  if random(0.0 .. 1.0) < obstacle_chance:
    var obstacle_position = random(0 .. len(game_board) - 2)
    game_board[obstacle_position] = '#'

for i in 1..5:
  generate_obstacle()

print_board()
```

Save the file and run the command nim c -r game.nim again. This will compile and run the game with obstacles added to the board.

## Exercise 4: Collision Detection ##
In this exercise, you will add collision detection to the game. If the player collides with an obstacle, the game will end. Copy the following code into game.nim:

```
proc check_collision() =
  if game_board[player_position] == '#':
    echo "Game over!"
    quit()

while true:
  check_collision()
  var input = readLine(stdin)
  if input == "q":
    break
  elif input == "left":
    move_player("left")
  elif input == "right":
    move_player("right")
  generate_ob
```
