# Dinogame
The endless-runner mechanics were implemented using a physics-based system for gravity, jumping, and ducking. Obstacles are generated at pseudo-random intervals with increasing velocity to scale difficulty, while real-time collision detection ensures precise interaction. The program tracks the score based on survival time and manages game states 

# Features:

Real-time Physics: Implements gravity, vertical velocity, and collision detection.

Variable Obstacles: Includes static cacti and flying birds with different heights.

Dynamic Difficulty: Game velocity increases over time, making it harder to survive.

Frame-Independent Movement: Uses Delta Time to ensure the same game speed regardless of the computer's frame rate.

State Management: Handles "Running", "Jumping", "Ducking", and "Game Over" states.

# How it works:

Input Handling: The player uses SPACE or UP to jump and DOWN to duck.

Obstacle Generation: Obstacles are spawned at pseudo-random intervals and move towards the left at a set velocity.

Collision Logic: The program constantly checks if the dinosaur's hitbox overlaps with an obstacle's hitbox.

Score System: The score is calculated based on survival time and is updated in real-time on the display.

# How to Install:

Make sure you have Python installed and the Pygame library:

		pip install pygame


# How to Run:

Save the code in a file named main.py and run it using:

	python main.py


# Controls:

SPACE / UP: Jump

DOWN (Hold): Duck (reduces height to avoid birds)

SPACE (after Game Over): Restart game

# Code Overview

## Key Classes & Functions:
Dinosaur Class: Manages the player's position, physics (gravity/velocity), and ducking state.

Obstacle Class: A base class for cacti and birds, handling their movement and screen exit removal.

init_game: Resets all variables, scores, and obstacle lists for a new session.

main (Game Loop): The heart of the program that handles events, updates positions, checks for collisions, and renders graphics at 60 FPS.

## Dinogame Logic:

The jump mechanic follows the formula:$$y_{pos} = y_{pos} + (velocity \cdot \Delta t)$$Where velocity is modified by gravity:$$velocity = velocity + (gravity \cdot \Delta t)$$
