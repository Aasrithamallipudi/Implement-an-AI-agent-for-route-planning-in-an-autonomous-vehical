Implement an AI Agent for Route Planning in an Autonomous Vehicle

 1️. Objective

This project focuses on simulating how an autonomous vehicle decides the best route to take in a constantly changing environment.
The idea is simple: use the **A*** search algorithm to plan a path while dealing with:

* Roadblocks
* Traffic-heavy regions
* Moving cars that appear as temporary obstacles

The goal is to show how an AI agent reacts and adjusts as it moves through the grid.

 2️. Environment

The simulation is built on a **20×20 grid**. Each cell represents a piece of road, and every cell behaves differently based on what it contains.

 **Types of Cells**

* Normal road — cost 1
* Static traffic zone — cost 5
* Roadblock — cannot pass through it
* Moving cars — dynamic obstacles that shift around during the simulation

 **How the Environment Behaves**

* Cars move every step, so the situation keeps changing
* The agent follows the A* path that was calculated at the start
* If a moving car enters the next step on the path, the simulation reacts immediately
* The grid updates visually as the agent moves

 **Libraries Used**

* NumPy
* Matplotlib
* Random
* Heapq
* IPython Display

All the movement and updates make the environment feel active rather than static.


3️. Algorithm Used — A* Pathfinding

A* is used to figure out the shortest and least-cost path from the start to the goal.

 **Main Points**

* Manhattan distance is used as the heuristic
* The algorithm naturally avoids:

  * Roadblocks
  * Moving cars
  * High-cost traffic zones
* A priority queue ensures the most promising cell is explored first
* Once the goal is reached, the path is reconstructed and displayed

 **Dynamic Behavior**

As the agent moves:

* Cars continue shifting positions
* If one of them blocks the next cell, the simulation stops
* Every step is shown visually, making the movement easy to follow



4️. Results

 ✔️ Path Generation

The system automatically picks a start and goal and calculates a valid path using A*.

 ✔️ Live Movement

During navigation:

* Each move is shown on the grid
* Cars move at the same time
* Depending on the situation:

  * The agent reaches the goal, or
  * A moving car blocks the path

 ✔️ Visual Output

The simulation displays:

* Start and goal
* Roadblocks
* Traffic zones
* Moving cars
* The planned A* route

The animation updates roughly every 0.5 seconds.


5️. How to Run the Project

 👉 Running in Google Colab

1. Open the notebook in Colab
2. Run all the cells
3. The simulation will:

   * Generate the grid
   * Pick start and goal
   * Compute the A* path
   * Show the step-by-step movement

Colab refreshes the output using `clear_output()`.

 💻 Running Locally

Install the required libraries:

```bash
pip install numpy matplotlib
```

Then run:

```bash
python autonomous_navigation_dynamic_grid.py
```

 6️. Developer’s Role

This project includes:

* Creating the grid and its behavior
* Writing the A* pathfinding algorithm
* Adding moving obstacles
* Displaying the simulation using Matplotlib
* Handling collision situations
* Splitting the code into clear, understandable functions

**Skills Demonstrated**

* Path planning
* Search algorithms
* Simulation design
* Visualization
* Real-time environment handling

