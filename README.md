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
