# NCDC Weekly Task — Conway's Game of Life

## Course
**NCDC Cohort 02/2025 — Design Verification (DV)**
NUST Chip Design Centre (NCDC), NUST

## Module
**C/C++ Module** — Weekly Task

---

## Overview

This project implements **Conway's Game of Life** entirely in C. Conway's Game of Life is a classic zero-player cellular automaton where the state of a grid evolves generation by generation based on a fixed set of rules applied to each cell and its eight neighbours. The simulation explores concepts of emergence, pattern recognition, and efficient grid traversal in C.

---

## Rules of the Game

Every cell in an infinite two-dimensional grid is either **alive** or **dead**. At each time step, the following transitions are applied simultaneously to every cell:

1. A live cell with **fewer than 2** live neighbours dies (underpopulation).
2. A live cell with **2 or 3** live neighbours survives to the next generation.
3. A live cell with **more than 3** live neighbours dies (overpopulation).
4. A dead cell with **exactly 3** live neighbours becomes alive (reproduction).

---

## Implementation Details

- **Language:** C (C99 standard)
- **Grid representation:** 2D character array with boundary wrapping
- **Input formats:** Plaintext grid files (e.g., `.txt` files with `*` for alive and `.` for dead)
- **Pattern support:** Glider, Spaceship (sship), and custom world files
- **Output:** Successive generation states printed to stdout or written to file

### Key Source Files

| File | Description |
|------|-------------|
| `lifegame.c` | Core simulation engine — applies the Game of Life rules each generation |
| `lifegame.h` | Header file — data structures and function declarations |
| `lab1a.c` | Part A implementation — basic grid reading and single-step evolution |
| `lab1b.c` | Part B implementation — multi-generation loop with terminal rendering |
| `gameOflifeB` | Compiled binary for the Game of Life simulation |
| `lifegcleame` | Alternate compiled binary with cleaned output formatting |
| `glider.txt` | Classic glider pattern input file |
| `sship.txt` | Spaceship pattern input file |
| `sshipout.txt` | Expected output for the spaceship pattern |
| `world.txt` | General test world input |
| `Weekly Task report.docx` | Written report documenting design choices and test results |

---

## How to Build and Run

```bash
# Compile
gcc -o lifegame lifegame.c -Wall

# Run with a pattern file
./lifegame glider.txt 10        # Simulate 10 generations of the glider
./lifegame world.txt 50         # Simulate 50 generations of a custom world
```

---

## Patterns Included

- **Glider** — A pattern that moves diagonally across the grid.
- **Spaceship (sship)** — A horizontally travelling pattern.
- **Custom World** — A user-defined initial configuration for open-ended exploration.

---

## Concepts Demonstrated
- 2D array manipulation in C
- Neighbour-counting with boundary conditions
- File I/O for reading initial grid states
- Iterative simulation loops
- Terminal-based visualisation of evolving patterns
