# SUTD 50.002 FPGA arcade machine

A two-player, three-lane browser arcade prototype for exploring a Subway Surfers-style physical cabinet. Players dodge falling cubes while the game speeds up; the longer survival time wins. The visual direction draws on the **Nano Banana** physical Subway Surfers cabinet.

The repository name reflects the intended **SUTD 50.002 FPGA arcade-machine context**. The source currently contains a browser game and two sprite-animation studies. It does not include HDL, board constraints, hardware integration or an FPGA build procedure.

## Play the browser prototype

Open [`index.html`](index.html) directly in a modern browser. No package installation, server or build step is required. The existing hosted game uses [GitHub Pages](https://neonat.github.io/sutd-50002-fpga-arcade-machine/).

| Player | Move left | Move right |
| --- | --- | --- |
| P1 | `A` | `D` |
| P2 | `←` | `→` |

Press `Space` to start or restart. On-screen buttons also accept mouse and touch input.

Each player has a three-lane grid. A cube reaching the bottom of the player's current lane ends that player's run. The session continues until both players are out, then compares their survival times. The game includes logic to leave a safe lane near the bottom.

## What is implemented

- Two players with separate lane positions, obstacle grids and survival timers.
- Falling obstacles, increasing speed, collision handling, restart and winner display.
- Canvas-based dot-matrix player sprites and CSS neon effects.
- Separate monochrome running and strafing animation studies.

The implementation uses vanilla HTML, CSS and JavaScript. [Orbitron](https://fonts.google.com/specimen/Orbitron) and [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono) supply the arcade typography; loading those Google Fonts requires a network connection.

## Source guide

| File | Purpose |
| --- | --- |
| [`index.html`](index.html) | Main two-player game, including interface, styles and game loop. |
| [`8x8_runner_bw.html`](8x8_runner_bw.html) | Monochrome runner animation study. |
| [`8x8_runner_strafe.html`](8x8_runner_strafe.html) | Running and strafing animation study. |

## Context and status

The cabinet reference uses a 3×5 grid of backlit amber cubes per player, a dot-matrix lane indicator and physical arcade buttons. This repository explores that interaction in a browser; it is not a record of completed FPGA hardware.

The existing roadmap includes sound effects, scoring beyond survival time, an animated in-game walk cycle, persistent high scores and further mobile layout work. There is no automated test suite or hardware verification flow checked in.

## License

The existing project documentation declares the MIT License. A standalone `LICENSE` file is not included in the current repository.
