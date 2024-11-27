Pathfinding Algorithms Visualization
This project visualizes two popular pathfinding algorithms: A (A-star)* and Dijkstra. It uses Pygame to create a grid-based environment where you can observe how these algorithms find the shortest path from a start point to an end point while avoiding obstacles (walls).

Files in this Repository
pathfinding_utils.py: Contains shared utilities, such as the Spot class, grid creation, and visualization functions.
astar.py: Implements the A (A-star)* algorithm.
dijkstra.py: Implements the Dijkstra algorithm.
Prerequisites
To run this project, you need the following Python packages:

pygame: For graphical user interface and visualizations.
You can install it using pip:

bash
Copy code
pip install pygame
How to Run
Clone the repository:

bash
Copy code
git clone <repository-url>
cd pathfinding-visualization
Run A algorithm*:

To run the A algorithm*, execute the following command:

bash
Copy code
python astar.py
Run Dijkstra algorithm:

To run the Dijkstra algorithm, execute the following command:

bash
Copy code
python dijkstra.py
Features
Interactive Grid: The grid consists of a grid of squares where you can:

Left-click to place the start point.
Right-click to place the end point.
Left-click to place barriers (walls).
Right-click to remove barriers or reset the start and end points.
Algorithms:

A Algorithm*: Uses a heuristic to efficiently find the shortest path.
Dijkstra Algorithm: Finds the shortest path by exploring all nodes systematically.
Maze-like Fixed Map: Both algorithms are initialized with a predefined maze (barriers) to test the algorithms with fixed walls.

Customizing the Map
If you want to modify the maze or the start/end points, you can edit the code directly in the astar.py and dijkstra.py files. The start and end points are predefined at the following positions:

Start Point: (10, 10)
End Point: (40, 40)
You can also modify the maze by changing which grid points are designated as barriers. In the provided code, barriers are added with this line in both algorithms:

python
Copy code
for i in range(20, 30):
    grid[i][25].make_barrier()
This adds a vertical wall between rows 20 and 30 at column 25.

Visual Output
The visualization will display a grid where:

Start Point: Orange
End Point: Turquoise
Barriers: Black
Path: Purple (once the algorithm finds it)
Open nodes: Green
Closed nodes: Red
Example Screenshots
A* Algorithm

Dijkstra Algorithm

How to Add Your Own Images
To add your own images of the visualizations:

Run either the astar.py or dijkstra.py script to generate the pathfinding visualization.
Take a screenshot of the Pygame window showing the grid and pathfinding process.
Save the screenshot image(s) and add them to this repository.
Replace the placeholder paths path/to/astar_example_image.png and path/to/dijkstra_example_image.png in the README with the relative paths to your images.
Algorithm Descriptions
A* Algorithm
The A algorithm* is a pathfinding algorithm that finds the shortest path from a start point to an end point. It uses the following two values to determine the best path:

g-score: The cost of the path from the start to the current point.
f-score: The estimated total cost (g-score + heuristic) to reach the goal.
The A* algorithm uses a priority queue to explore nodes with the lowest f-score first. It incorporates a heuristic function to make the search more efficient by prioritizing paths that appear to lead toward the goal.

Dijkstra Algorithm
The Dijkstra algorithm finds the shortest path from a starting point to all other points in the grid. Unlike A*, it does not use a heuristic function but instead explores nodes in increasing order of their distance from the start. It is guaranteed to find the shortest path but can be less efficient than A* in certain situations.

Troubleshooting
No Pygame Window: Make sure that you have the pygame package installed.
Slow Performance: If the algorithm runs slowly, consider reducing the grid size by modifying the ROWS variable in astar.py or dijkstra.py (default is 50).
License
This project is licensed under the MIT License - see the LICENSE file for details.

