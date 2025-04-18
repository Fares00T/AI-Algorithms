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

---

# 2- 📊 Clustering Algorithms: Hard C-Means (HCM) and Fuzzy C-Means (FCM)

This project demonstrates two popular clustering algorithms — **Hard C-Means (HCM)** and **Fuzzy C-Means (FCM)** — applied to simple 2D data.

### 🧠 What Are These Algorithms?

#### 1. Hard C-Means (HCM)

Also known as **k-means**, this is a crisp clustering algorithm where each data point belongs to exactly one cluster.

**How it works:**

- Initialize a partition matrix or random labels.
- Compute cluster centroids based on assignments.
- Assign each point to the nearest centroid.
- Repeat until convergence (centroids stop changing significantly).

**Extras:**

- Calculates a **Quality Index (J-index)** — lower is better.
- Tracks centroid changes using a rotation matrix.
- Visualizes final clusters using `matplotlib`.

🔁 Example function: `hcm(X, labels, num_clusters)`

---

#### 2. Fuzzy C-Means (FCM)

A **soft clustering** algorithm where each point belongs to all clusters to a certain degree.

**How it works:**

- Assign fuzzy memberships (values from 0 to 1).
- Iteratively update centroids and membership values.
- Uses a **fuzziness coefficient `m`** to control overlap.

**Evaluation:**

- `jm`: Objective function (lower is better).
- `fpc`: Fuzzy Partition Coefficient (higher = clearer clustering).

🔁 Example function: `run_fcm_and_plot(X, c_values=[2, 3])`

---

## 🔍 Dataset

Both algorithms use a simple 2D dataset of 8 points:

```python
X = np.array([[x1, x2, ..., x8],
              [y1, y2, ..., y8]])
```

## Evolution Strategies for Model Parameter Optimization

This project implements an Evolution Strategy (ES) algorithm in Python to optimize the parameters of a non-linear regression model. The goal is to minimize the Mean Squared Error (MSE) between actual and predicted outputs using self-adaptive mutation techniques.

### 🧠 Model Equation

The model used to fit the data is:

output = a * (input^2) - b * cos(c * π * input)

## ⚙️ Features

- Evolution Strategy with self-adaptive mutation
- Minimizes MSE over generations
- Visual comparison between actual and approximated data
- Adjustable population size, max iterations, and convergence threshold

## 📈 Output

- Best-fit parameters `a`, `b`, and `c`
- Final MSE
- Runtime and iteration count
- Plot of actual vs. approximated values

## 🛠️ Usage

1. Make sure `numpy`, `matplotlib`, and your `mse_value()` function are defined/imported.
2. Call the `evolutionary_strategies()` function with:
   ```python
   solution = evolutionary_strategies(pop, N_max, epsilon, input_data, output_data)





