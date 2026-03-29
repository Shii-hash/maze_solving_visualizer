# maze_solving_visualizer
# Pathfinding Algorithm Visualizer

A real-time visualizer that generates random mazes and solves them using three classic AI search algorithms — A*, Breadth-First Search, and Depth-First Search.

---

## The Problem It Solves

Pathfinding is a fundamental problem in AI — used in GPS navigation, game AI, robotics, and network routing. Understanding *how* different algorithms explore a search space, and *why* some find optimal paths while others don't, is a core concept in AI education. This project makes those differences visible and intuitive through real-time animation.

---

## Algorithms Implemented

| Algorithm | Strategy | Optimal Path? | Uses Heuristic? |
|---|---|---|---|
| **A\*** | Best-first (f = g + h) | ✅ Yes | ✅ Manhattan distance |
| **BFS** | Level-by-level expansion | ✅ Yes | ❌ No |
| **DFS** | Deepest node first | ❌ No | ❌ No |

---

## Features

- Random maze generation using the **Recursive Backtracker** algorithm
- Real-time step-by-step animation of each algorithm
- Color-coded visualization — frontier, visited nodes, and final path
- Live stats — nodes visited and path length
- Compare algorithms on the same maze by pressing 1, 2, 3
- Adjustable maze size and animation speed via CLI

---

## Requirements

- Python 3.8+
- A display (monitor)

---

## Setup

```bash
git clone https://github.com/<your-username>/maze-solver.git
cd maze-solver
pip install -r requirements.txt
```

---

## How to Run

```bash
# Default (21x21 maze, medium speed)
python maze_solver.py

# Custom maze size
python maze_solver.py --size 31

# Animation speed
python maze_solver.py --speed fast
python maze_solver.py --speed slow

# Combine
python maze_solver.py --size 25 --speed fast
```

---

## Controls

| Key | Action |
|---|---|
| `1` | Run A* Search |
| `2` | Run Breadth-First Search |
| `3` | Run Depth-First Search |
| `R` | Generate new random maze |
| `SPACE` | Pause / Resume |
| `ESC` | Quit |

---

## CLI Options

| Flag | Default | Description |
|---|---|---|
| `--size N` | 21 | Maze grid size (odd number recommended) |
| `--speed` | medium | Animation speed: `slow`, `medium`, `fast` |

---

## Project Structure

```
maze-solver/
├── maze_solver.py    # Main application
├── requirements.txt  # Dependencies
└── README.md         # This file
```

---

## How It Works

1. **Maze Generation** — Recursive Backtracker (DFS-based) carves passages through a grid of walls, producing a perfect maze with exactly one path between any two points.
2. **Algorithm runs** — The selected algorithm explores the maze step by step, yielding its current state (visited nodes, frontier) at each step.
3. **Visualization** — Pygame renders each state in real time, color-coding visited nodes, the active frontier, and the final solution path.
4. **Comparison** — Running different algorithms on the same maze shows clearly why A* visits far fewer nodes than BFS, and why DFS finds a path quickly but not optimally.
