# pingpong_using_lua
# Pong Game README.md

This README.md file provides an overview and explanation of the code for the classic Pong game created using the LÖVE2D framework with Lua. The game simulates a simple two-player Pong game where each player controls a paddle to hit the ball and score points.

## Getting Started

### Prerequisites

To run the Pong game, you need to have [LÖVE2D](https://love2d.org/) installed on your system. LÖVE2D is a framework for creating 2D games and applications using Lua scripting language.

### Running the Game

1. Download and install LÖVE2D from [here](https://love2d.org/).
2. Clone or download the repository containing the Pong game code.
3. To start the game, drag and drop the folder containing the game files onto the LÖVE2D executable, or run the following command in the terminal:

```bash
love /path/to/pong-game
```

## Game Description

Pong is a simple 2D tennis-like game where two players control paddles and try to hit the ball back and forth to score points. The ball moves between the players' paddles and the screen edges, and the player who fails to hit the ball loses a point. The first player to reach a score of 10 wins the game.

## Controls

Player 1:
- Move up: Press 'a'
- Move down: Press 'd'

Player 2:
- Move up: Press the right arrow key
- Move down: Press the left arrow key

During the game, press 'Enter' to serve the ball, restart the game, or continue after a point is scored.

## Code Structure

The Pong game is built using Lua and organized into several modules:

### Main.lua

- This file is the entry point of the game and contains the `love.load()`, `love.update()`, `love.draw()`, and `love.keypressed()` functions.
- The `love.load()` function is used to initialize the game, including setting up fonts, sounds, and screen settings.
- The `love.update()` function is called every frame and updates the game logic, including ball movement, collision detection, and score tracking.
- The `love.draw()` function is called every frame to render the game, including paddles, ball, scores, and UI messages.
- The `love.keypressed()` function handles keyboard input, allowing players to move their paddles and start/restart the game.

### Push.lua

- This file is a library called Push that handles resolution and scaling for different screen sizes.
- It is used to maintain a consistent virtual resolution while allowing the game to be displayed on various screen sizes.

### Class.lua

- This file is another library called Class that provides Object-Oriented Programming capabilities.
- It is used to define the Paddle and Ball classes, representing the player paddles and the game ball, respectively.

### Paddle.lua

- This file contains the `Paddle` class, which stores position and dimensions for each paddle and the logic for rendering them.
- It defines the methods `Paddle:init()` for initialization and `Paddle:update(dt)` for updating the paddle's position.

### Ball.lua

- This file contains the `Ball` class, which represents the game ball and its mechanics.
- It defines the methods `Ball:init()` for initialization, `Ball:update(dt)` for updating the ball's position, and `Ball:collides(paddle)` for detecting collisions with paddles.

### Fonts and Sounds

- The game uses three different fonts for different UI elements and sound effects for paddle-ball collision, scoring, and wall hits.

## Game States

The game progresses through different states, affecting the gameplay and UI messages:

1. `start`: The game starts in this state, displaying a welcome message and instructions to press 'Enter' to begin.
2. `serve`: In this state, the game displays a message indicating which player's turn it is to serve. Press 'Enter' to serve the ball and transition to the `play` state.
3. `play`: The main gameplay state where the ball is in play, and players control their paddles. No UI messages are displayed in this state.
4. `done`: This state is triggered when a player wins the game by reaching a score of 10. A victory message is displayed, and players can press 'Enter' to restart the game.

## Acknowledgments

The Pong game code was created by [your name here]. The game is built using the LÖVE2D framework and makes use of external libraries for resolution handling (Push) and object-oriented programming (Class). The fonts used in the game are licensed for use in this project. Sound effects were obtained from [source here] and are used with permission.

## License

This project is licensed under the [MIT License](LICENSE). You are free to modify and distribute the code, but please provide proper attribution to the original creator. Sound files used in this project have separate licensing terms and are not covered under this license.
