# Snake & Tetris Games

## Overview

Interactive implementations of classic games—Snake and Tetris—built with Python and Tkinter to practice object-oriented programming concepts including inheritance, encapsulation, and graphics rendering.

## Games Included

### Snake Game
Navigate your snake through a grid avoiding obstacles (white pixels) while collecting strawberries (red pixels). The snake grows with each berry eaten.

**Features:**
- Directional movement with arrow keys
- Periodic boundaries (wrap around edges)
- Obstacle avoidance and fruit collection
- Pause functionality
- Win/lose conditions

**Technologies:** Python, Tkinter, NumPy

### Tetris Game
Classic Tetris gameplay with custom Tetromino shapes falling from the top. Rotate, move, and stack pieces to clear rows.

**Features:**
- 7 unique Tetromino shapes with rotation
- Left/right movement and hard drop
- Row clearing and detection
- Game over detection
- Periodic gameplay mechanics

**Technologies:** Python, Tkinter, NumPy

## Core Architecture

**Key Classes:**
- `Pixel` - Individual grid squares with position, color, and movement
- `Grid` - Grid system managing obstacles and collectibles
- `Tetrominoes` - Parent class for game pieces with rotation patterns
- `Snake` - Snake game logic (inherits from Grid)
- `Tetris` - Tetris game logic (inherits from Grid)

## How to Run
```bash
python Snake.py    # Play Snake
python Tetris.py   # Play Tetris
```

## Controls

**Snake:**
- Arrow keys: Change direction
- P: Pause/resume
- D: Clear canvas

**Tetris:**
- Arrow keys: Move left/right, hard drop
- Up arrow: Rotate piece
- P: Pause/resume

## Learning Outcomes

- Object-oriented design with inheritance and encapsulation
- Graphics programming with Tkinter
- Event-driven programming (keyboard input handling)
- Algorithm implementation (collision detection, grid management)
- Game state management

## Project Structure
```
.
├── Pixel.py
├── Grid.py
├── Snake.py
├── Tetrominoes.py
├── Tetris.py
└── README.md
```
