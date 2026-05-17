# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is **Fruity Bird** - a Flappy Bird variant with special fruit abilities. It's a pure HTML5 Canvas game written in vanilla JavaScript, no build system required.

## Code Architecture

**All game code is contained in a single file:** `index.html`

The code is organized into classes, each responsible for a specific game system:
- `Background` - Visual background with stars, clouds, decorations
- `Bird` - Player character with physics and animation
- `BirdClone` - Helper clone that scores points for player
- `Pipe` - Individual obstacle pipe
- `PipeManager` - Spawns and manages pipes
- `Fruit` - Collectable fruit with special abilities
- `FruitManager` - Spawns and manages fruits
- `AbilityManager` - Tracks active fruit abilities and durations
- `UI` - User interface and button handling
- `Game` - Main game loop and state management

## Common Development Tasks

### Running the Game
The simplest way is to just open `index.html` directly in a web browser.

For a better development experience, you can serve it with any HTTP server:
```bash
# Python 3
python -m http.server 8000

# Node.js (if available)
npx serve .
```

Then visit http://localhost:8000 in your browser.

### Making Changes
Just edit `index.html` directly and refresh the browser. No build step required.

## Game Configuration

**Fruit Types** (10 total):
- gravity (🍎) - reverses gravity
- speed (🍊) - increases bird speed
- slow (🍋) - slows pipes
- invincible (🍇) - pass through pipes
- doubleScore (🍓) - double points
- magnet (🍑) - attracts fruits
- shrink (🍒) - smaller bird
- giant (🍉) - bigger bird
- freeze (🍈) - pipes stop moving
- clone (🥝) - clone helper

**Difficulty Levels:**
- easy - large gaps, slow speed
- normal - standard difficulty
- hard - small gaps, fast speed

## Git Operations
The repository is already initialized and connected to: https://github.com/XYStarU/fruity_bird
