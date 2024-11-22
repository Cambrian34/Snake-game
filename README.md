# Snake Game

This project implements a classic **Snake Game** using JavaScript and the HTML5 Canvas API. Players control a snake that grows longer as it eats apples, avoiding collisions with the edges of the game area.

---

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Controls](#controls)
4. [How to Run](#how-to-run)
5. [Code Structure](#code-structure)
6. [Potential Improvements](#potential-improvements)
7. [License](#license)

---

## Overview

**Author:** Alistair Chambers  
**Date:** 12/15/21  
**File:** `snake.js`  

The snake moves continuously, eating apples to grow longer. The player must guide the snake without hitting the edges of the canvas. The game includes a scoring system and supports pausing or restarting the gameplay.

---

## Features

- **Smooth Gameplay:** Continuous movement with a simple game loop.
- **Apple Respawn:** Apples appear at random locations, avoiding the snake’s body.
- **Collision Handling:** The snake wraps around the canvas edges.
- **Score Tracking:** Displays the player's score based on the snake's length.
- **Pause/Restart:** Players can pause the game or restart with a new snake.

---

## Controls

- **Arrow Keys:** Move the snake.
- **Shift Key:** Pause/Unpause the game.
- **Spacebar:** Reset the game.

---

## How to Run

1. Download the project files.
2. Open the `index.html` file in a modern browser.
3. The game will start automatically. Use the controls to play.

---

## Code Structure

### Classes

#### `Snake`
Represents the snake, including its position, size, and movement logic.

- **Attributes:**
  - `x`, `y`: Starting position.
  - `size`: Size of each segment.
  - `tail`: Array storing the snake's body segments.
  - `rotateX`, `rotateY`: Direction of movement.

- **Methods:**
  - `move()`: Updates the snake's position based on its direction.

#### `Apple`
Handles the apple's random placement, ensuring it doesn't spawn on the snake's body.

- **Attributes:**
  - `x`, `y`: Position.
  - `size`: Size of the apple.
  - `color`: Appearance.

### Core Functions

- `gameLoop()`: Starts the main game loop.
- `update()`: Updates game elements like snake movement and collision detection.
- `draw()`: Renders the game elements on the canvas.
- `checkHitWall()`: Wraps the snake around the canvas edges.
- `eatApple()`: Checks if the snake eats the apple and grows its tail.
- `createRect(x, y, width, height, color)`: Draws rectangles for game elements.

### Event Listeners

- `keydown`: Handles player input for movement, pausing, and restarting.

---

## Potential Improvements

1. **Game Over Mechanic:** End the game when the snake collides with itself.
2. **Difficulty Levels:** Increase speed as the score increases.
3. **Graphics Enhancements:** Add textures or animations.
4. **High Scores:** Track and display the top scores.
5. **Mobile Support:** Add touch controls for mobile devices.

---

## License

This project is open-source and can be used or modified under the terms of the MIT License.

---
