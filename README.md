# Two-player arcade cabinet prototype | SUTD 50.002

Two players dodge falling cubes on adjacent three-lane grids. Each player can move only left or right. When a cube reaches a player's lane at the bottom, their timer stops and the other player can keep going. The longer survival time wins. [Play the browser prototype](https://neonat.github.io/sutd-50002-fpga-arcade-machine/).

The design draws on the Nano Banana physical Subway Surfers cabinet. Its backlit cube grid, button controls, and dot-matrix lane indicator gave the SUTD 50.002 FPGA arcade-machine project a concrete interface to try in software. This repository contains the browser game and sprite studies. No HDL, board constraints, or completed hardware build are included.

## Play locally

Open [index.html](index.html) in a browser. Press **Space** to start or restart. Player 1 uses **A** and **D**. Player 2 uses the **left** and **right** arrow keys. The on-screen lane buttons also accept mouse and touch input. The page runs directly from the file. It requests the optional Orbitron and Share Tech Mono fonts from Google Fonts.

## How the cabinet maps to the browser

| Cabinet element | Browser implementation |
| --- | --- |
| Backlit cubes | CSS Grid lays out three columns and five rows per player. JavaScript advances the obstacles and checks whether a cube hits the player's lane. |
| Lane indicator | A small HTML canvas draws the player's dot-matrix figure. Moving changes the lane shown beneath the grid. |
| Arcade buttons | Keyboard and pointer input call the same lane movement functions, which stop at the outer edges. |
| Survival timer | A shared JavaScript game loop advances both grids. It shortens the delay between ticks as the round progresses and compares the final times after both players are out. |

The [monochrome runner](8x8_runner_bw.html) and [strafing runner](8x8_runner_strafe.html) are standalone animation studies. Open either file to inspect the motion separately from the game. The repository contains no automated test suite.

## Licence

Earlier project documentation identifies the MIT License. The repository does not include a standalone licence file.
