# 🕹️ Subway Surfers Arcade

A two-player browser arcade game inspired by the **Nano Banana** physical Subway Surfers cabinet. The main game lives in `index.html` and runs directly in a browser.

Despite the repository name `subway-surfers-fpga`, the current source is a browser game and sprite-animation studies. FPGA HDL, board constraints and hardware build instructions are not included.

![Game Theme](https://img.shields.io/badge/theme-TRON%20arcade-00f0ff?style=flat-square) ![Players](https://img.shields.io/badge/players-2-39ff14?style=flat-square) ![File](https://img.shields.io/badge/single%20file-HTML-orange?style=flat-square)

---

## 🎮 How to Play

Each player controls a character on a **3-lane grid**. Glowing cubes fall down the lanes — dodge them or you die. The game speeds up over time, just like Subway Surfers. Last player standing wins.

### Rules
- Cubes fall from the top and disappear at the bottom
- If a cube reaches the bottom of **your lane**, you die
- Multiple cubes fall at once, but there is **always at least one safe lane**
- No lives — one hit and you're out
- The session ends when **both players** have died
- Winner is whoever survived longest

---

## ⌨️ Controls

| Player | Move Left | Move Right |
|--------|-----------|------------|
| P1     | `A`       | `D`        |
| P2     | `←`       | `→`        |

Press `Space` to start or restart.

On-screen buttons also work for touch/mouse.

---

## 🚀 Play It

### Option 1 — Open locally
Download `index.html` and open it in any browser. That's it.

### Option 2 — Play online

Open the existing [GitHub Pages game](https://neonat.github.io/subway-surfers-fpga/).

---

## 🗂️ Project Structure

```
/
├── index.html               # main two-player game
├── 8x8_runner_bw.html       # monochrome runner animation study
├── 8x8_runner_strafe.html   # running/strafe animation study
└── README.md
```

---

## 🔧 Built With

- Vanilla HTML / CSS / JavaScript; no package installation or build step
- Optional Google Fonts require a network connection
- [Orbitron](https://fonts.google.com/specimen/Orbitron) — display font (Tron aesthetic)
- [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono) — monospace UI font
- Canvas API — dot-matrix player sprite
- CSS animations — neon glow, scanlines, flicker effects

---

## 🖼️ Inspired By

The physical **Nano Banana** Subway Surfers arcade cabinet — a 3×5 grid of backlit amber cubes per player, with a dot-matrix display showing the player's lane position, and chunky green arcade buttons.

---

## 📋 Roadmap

- [ ] Sound effects
- [ ] Scoring system (beyond time survived)
- [ ] Animated sprite walk cycle on the dot-matrix
- [ ] High score persistence
- [ ] Mobile layout optimisation

---

## 📄 License

MIT — do whatever you want with it.
