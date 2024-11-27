
# Pathfinding Visualization Project

Welcome to the **Pathfinding Visualization Project**! This tool visualizes two popular pathfinding algorithms: **A*** (A-Star) and **Dijkstra's Algorithm**. The application uses Pygame to display the grid and simulate the algorithms as they find paths between the selected start and end points.

---

## Visual Demonstration

<p align="center">
  <img src="path/to/astar_demo.gif" alt="A* Algorithm Demo" width="45%" />
  <img src="path/to/dijkstra_demo.gif" alt="Dijkstra Algorithm Demo" width="45%" />
</p>

---

## Features

- **Visualize Pathfinding Algorithms**:
  - **A\***: A heuristic-based search algorithm.
  - **Dijkstra's Algorithm**: A non-heuristic shortest-path algorithm.
  
- **Interactive Grid**:
  - Set start and end points.
  - Create barriers to test algorithm performance.
  - Reset grid for repeated testing.

- **Real-Time Visualization**:
  - Watch the algorithms explore the grid and find optimal paths.

---

## Running the Application

### Prerequisites

Ensure you have Python installed (version 3.7 or higher). Install the required library using:

```bash
pip install pygame
```

### Steps to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your_username/pathfinding-visualizer.git
   cd pathfinding-visualizer
   ```

2. Run the program:

   ```bash
   python main.py
   ```

3. Use the controls below to interact with the grid and visualize the algorithms.

---

## How It Works

### Controls

- **Grid Interaction**:
  - **Left Click**: Set the start, end, or barriers.
  - **Right Click**: Remove an obstacle, start, or end.

- **Keyboard**:
  - **SPACE**: Start the selected algorithm.
  - **C**: Reset the grid.

### Algorithms

1. **A***:
   - Uses a heuristic function (Manhattan distance).
   - Combines the cost to reach a node and an estimated cost to the goal.
   - Faster for goal-oriented searches.

2. **Dijkstra's Algorithm**:
   - Computes the shortest path without using heuristics.
   - Explores all paths systematically.

---

## Visual Feedback

- **Green**: Nodes in the open set.
- **Red**: Nodes in the closed set.
- **Purple**: The final path.
- **Black**: Barriers.
- **Orange**: Start point.
- **Turquoise**: End point.

---

## Customization

### Changing Grid Size

Modify the `ROWS` and `WIDTH` constants in `main.py`:

```python
ROWS = 50  # Number of rows
WIDTH = 800  # Width of the window
```

---

## Project Structure

```
|-- pathfinding_util.py    # Utility functions and Spot class
|-- astar_algorithm.py     # A* implementation
|-- dijkstra_algorithm.py  # Dijkstra's implementation
|-- main.py                # Main script for running the visualization
```

---
