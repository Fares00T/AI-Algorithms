# AI-Algorithms
This repository contains a collection of various AI algorithms implemented in Python. It aims to provide a practical understanding of different machine learning and artificial intelligence techniques, from basic to advanced models.

## 1 - 🐜 Ant Algorithm - Traveling Salesman Problem

This implementation uses the **Ant Colony Optimization (ACO)** algorithm to solve the **Traveling Salesman Problem (TSP)**, where the goal is to find the shortest possible route that visits each city exactly once and returns to the starting point.

### 🔍 How it Works

- **Inspiration**: The algorithm mimics the foraging behavior of real ants. Ants leave behind pheromones on paths they take, which influence the decisions of other ants.
- **Initialization**: A set of ants is randomly placed on cities.
- **Tour Construction**: Each ant builds a tour by probabilistically choosing the next city based on two factors:
  - **Pheromone levels (τ)** – representing learned desirability.
  - **Heuristic information (η = 1/distance)** – favoring closer cities.
- **Pheromone Update**: After all ants complete their tours:
  - Pheromones evaporate slightly.
  - Ants deposit pheromones on their path, with better (shorter) tours getting more pheromone.
- **Best Path Tracking**: The shortest path found across all iterations is stored and displayed.

This simple yet powerful strategy allows the system to converge toward near-optimal solutions through collective learning and exploration.

### 📈 Visualization

The output includes a plotted graph showing the best tour found, with city indices, the path taken, and the start city highlighted.

---

🔧 Adjust parameters like `alpha`, `beta`, `ro`, and the number of ants/iterations to explore different behaviors and convergence speeds.
