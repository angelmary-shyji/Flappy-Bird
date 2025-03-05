# Flappy Bird Game in Java

This project is a simple implementation of the **Flappy Bird** game using Java and the Swing library. The game includes a bird that can jump, pipes that move from right to left, and a score system that tracks the player's progress. The game ends when the bird collides with a pipe or the ground.

## Key Features

1. **Game Loop**: The game runs in a continuous loop with a frame rate of 60 frames per second. The loop handles:
   - Moving the bird and pipes.
   - Checking for collisions.
   - Updating the game state (e.g., game over status, score).

2. **Graphics Rendering**: The game uses `JPanel` for rendering the game screen:
   - Background image.
   - Bird image.
   - Pipe images (both top and bottom pipes).
   - Score display.

3. **Bird Mechanics**:
   - The bird is controlled using the **spacebar** to make it "jump" (i.e., move upwards).
   - The bird is affected by gravity, and its movement is simulated using velocity. The bird falls after jumping due to gravity.
   - The bird can collide with pipes, resulting in a "game over" state.

4. **Pipe Mechanics**:
   - Pipes are placed randomly at different heights and move from the right to the left of the screen.
   - Each pipe pair (top and bottom pipes) creates a gap through which the bird must fly.
   - When the bird successfully passes through a pair of pipes, the player earns points.
   - Pipes are continuously generated using a timer.

5. **Collision Detection**:
   - A collision occurs when the bird overlaps with a pipe, either top or bottom, or when the bird goes below the screen.
   - The game ends if a collision is detected, and the game over screen is displayed.

6. **Score System**:
   - The score increases by 0.5 points for each pair of pipes the bird successfully passes.
   - The score is displayed at the top left of the screen.

7. **Game Restart**:
   - If the game is over, pressing the spacebar will restart the game by resetting the bird's position, clearing pipes, and setting the score back to zero.

## Files
- `FlappyBird.java`: Contains the main game logic, including bird and pipe behavior, collision detection, and game rendering.
- `App.java`: Initializes the game window (JFrame), adds the game panel (`FlappyBird`), and starts the game loop.

## Images
- `flappybirdbg.png`: Background image for the game.
- `flappybird.png`: Image of the bird.
- `toppipe.png`: Image of the top pipe.
- `bottompipe.png`: Image of the bottom pipe.

