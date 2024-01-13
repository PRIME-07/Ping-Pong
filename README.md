# Ping-Pong Game Documentation

## Introduction
This documentation provides an overview of the Ping-Pong game implemented in Python using the Pygame library. The game consists of two paddles and a ball that moves between them. The objective is to score points by hitting the ball past the opponent's paddle. Use <kbd>W</kbd> and <kbd>S</kbd> keys to control the left paddle and use <kbd>↑</kbd> and <kbd>↓</kbd> keys to move right paddle.

## Table of Contents
1. [Game Components](#game-components)
    - 1.1 [Paddle](#paddle)
    - 1.2 [Ball](#ball)
2. [Initialization](#initialization)
3. [Drawing and Display](#drawing-and-display)
4. [Collision Handling](#collision-handling)
5. [Paddle Movement](#paddle-movement)
6. [Main Game Loop](#main-game-loop)
7. [Winning Conditions](#winning-conditions)
8. [Conclusion](#conclusion)

## 1. Game Components <a name="game-components"></a>

### 1.1 Paddle <a name="paddle"></a>
- **Attributes:**
  - `x`, `y`: Current position of the paddle.
  - `original_x`, `original_y`: Initial position of the paddle.
  - `width`, `height`: Dimensions of the paddle.
- **Methods:**
  - `draw(win)`: Draws the paddle on the game window.
  - `move(up)`: Moves the paddle up or down based on the boolean parameter `up`.
  - `reset()`: Resets the paddle to its original position.

### 1.2 Ball <a name="ball"></a>
- **Attributes:**
  - `x`, `y`: Current position of the ball.
  - `original_x`, `original_y`: Initial position of the ball.
  - `radius`: Radius of the ball.
  - `x_vel`, `y_vel`: Velocity of the ball in the x and y directions.
- **Methods:**
  - `draw(win)`: Draws the ball on the game window.
  - `move()`: Moves the ball based on its velocity.
  - `reset()`: Resets the ball to its original position.

## 2. Initialization <a name="initialization"></a>
- Pygame is initialized, and essential variables such as window dimensions, paddle dimensions, ball radius, and fonts are defined.

## 3. Drawing and Display <a name="drawing-and-display"></a>
- The `draw` function is responsible for rendering the game components on the window.
- Paddles, the ball, and the scores are drawn on the window.

## 4. Collision Handling <a name="collision-handling"></a>
- The `handle_collision` function checks for collisions between the ball and the window boundaries, as well as with the paddles.
- If a collision is detected, the ball's velocity is adjusted accordingly.

## 5. Paddle Movement <a name="paddle-movement"></a>
- The `handle_paddle_movement` function handles the movement of both paddles based on keyboard input.
- Paddles move up or down based on the pressed keys.

## 6. Main Game Loop <a name="main-game-loop"></a>
- The main game loop controls the flow of the game.
- It updates the display, handles events, moves the ball, and manages paddle movement.

## 7. Winning Conditions <a name="winning-conditions"></a>
- The game continues until one player reaches the winning score (`WINNING_SCORE`).
- If a player wins, a victory message is displayed, and the game resets after a brief delay.

## 8. Conclusion <a name="conclusion"></a>
The Ping-Pong game implemented in Python using Pygame provides a simple yet engaging gaming experience. Players control paddles to bounce a ball back and forth, aiming to score points. The code structure is modular, making it easy to understand and extend. Feel free to customize the game further or enhance its features based on your preferences.