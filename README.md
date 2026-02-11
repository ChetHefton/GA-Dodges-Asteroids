# Genetic Alg. Dodges Asteroids (WIP)

A small browser game built with **Matter.js** where the player controls a ship and dodges incoming asteroid-like obstacles.  
Obstacles spawn continuously, speed increases over time, and score/level track progress.

This project is planned to become **neuroevolution-driven** (AI learns to dodge) in a future update.

---

## Current gameplay

- Player ship is a polygon body (Matter.js)
- “Asteroids” are random polygon shapes with spin and bounce
- Obstacles spawn off-screen and move left across the screen
- Score increases when obstacles pass off-screen
- Level increases as score grows
- Flame sprite animation renders behind the ship (frame-by-frame images)

---

## Controls

- **Left Arrow**: move left (also squishes the ship while held)
- **Right Arrow**: move right (also squishes the ship while held)

---

## Tech

- HTML / CSS / JavaScript
- Matter.js physics engine
- Canvas sprite animation (flame frames)

---

## How to run

Because the game loads assets (sprite frames), run it from a local server:

- VS Code “Live Server” extension, or
- Python:
  ```bash
  python -m http.server
Then open the page in your browser.

### Planned: Neuroevolution (next steps)

- Goal: train an agent to control the ship automatically.

# Planned approach:

- Replace keyboard input with NN outputs (up/down)

- Inputs could include:

    - player y position and velocity

    - distance to nearest obstacle

    - obstacle y position and relative speed

    - gap / safe path estimate

- Fitness:

    - survival time

    - score / distance traveled

 -Evolution:

    - select top agents

    - clone + mutate weights
