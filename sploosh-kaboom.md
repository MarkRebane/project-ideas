# Sploosh Kaboom

## The game

Sploosh Kaboom is a single player version of the classic game of Battleship from The Legend of Zelda: The Wind Waker, e.g. <https://youtu.be/Tj1u2X7iM2s>.

Unlike Battleship, which is played on two 11x9 boards, Sploosh Kaboom is played on a single 8x8 board, i.e. similar to a chess board. Hidden on the board are three large objects. Each object is in either a single column or a single row and each has a different length, i.e. two, three, or four grid squares long. The player has 24 shots to sink all the objects. To sink an object, every grid square that the object occupies must go kaboom! If the player sinks all the objects before they run out of shots, then they win; otherwise, they lose.

Kaboom:     *
Sploosh:    x
Last shot: (x) or (*)

- All player input is case-insensitive, e.g. y, N, yEs, nO, A5, e8

- A capital prompt indicates the default response if the player presses <enter>
  without any other input.
  
- If the player input is invalid, the game will indicate this and  prompt the
  player again, e.g.
  - `Unrecognised response 'blah'. Would you like to play Sploosh Kaboom? [Y/n]> _`
  - `Invalid coordinates 'watman'. Take a shot> _`
  - `Already fired at 'a4'. Take a shot> _`
  
- If the player wins:
  `You won in ## shots!`
  
- If the player loses:
  `You lose. Hit # objects and destroyed # objects.`
  Also, reveal the hidden objects to the player.

## Example Board:

```
Would you like to play Sploosh Kaboom? [Y/n]> _

|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 8
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 7
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 6 
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 5
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 4
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 3
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 2
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 1
|---+---+---+---+---+---+---+---|
  a   b   c   d   e   f   g   h

Shots remaining: 24

Take a shot> a4

Sploosh!

|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 8
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 7
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 6 
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 5
|---+---+---+---+---+---+---+---|
| x |   |   |   |   |   |   |   | 4
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 3
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 2
|---+---+---+---+---+---+---+---|
|   |   |   |   |   |   |   |   | 1
|---+---+---+---+---+---+---+---|
  a   b   c   d   e   f   g   h

Shots remaining: 23

Take a shot> _
```

## Objectives

### Primary

1. Write an interactive text-based game that randomly generates a board.
2. Write an automated test driver program that tests the game's mechanics.
    - HINT: Writing tests as you go will encourage you to write 'testable' software. Don't leave this until the end! It's significantly easier to test software that is designed to be testable.

### Secondary

Once all of the above is implemented, tested and working extend the game with more features and make it something you're proud to show people, i.e. a 'portfolio piece':
- add a scoreboard or high score (best score == fewest shots)
- track the total number of wins
- save and load the scoreboard and statistics using a file on disk
- record and replay the player's game
- add tests for all the above
- create a window, add basic graphics and make the game playable with the mouse (no keyboard input required)
- add sound effects and music
- add a network LAN multiplayer Vs mode of 2-player battleships
- whatever else you want!
