🚗🗺️ Autonomous Navigation in a Dynamic Grid Environment Using A*
1️⃣ Objective

The objective of this project is to simulate how an autonomous vehicle plans and navigates a route in a dynamic environment.
The system uses the A* algorithm to find an optimal path on a grid while avoiding:

Static obstacles (roadblocks)

High-cost traffic zones

Dynamic obstacles (moving cars)

The project demonstrates intelligent decision-making in real time, where the agent must respond to changes in the environment as it moves.

2️⃣ Environment

The simulation takes place in a 20×20 grid world, where each cell represents a road segment with different properties:

Grid Components

Normal Road (Cost = 1)

Static Traffic (Cost = 5)

Roadblock (Impassable)

Moving Cars (Dynamic obstacles)

Environment Behavior

Moving cars change position every step

The autonomous agent follows the planned A* path

If a moving car blocks the next move, the simulation reacts immediately

Libraries Used

NumPy (grid creation & handling)

Matplotlib (visualization)

Random (dynamic environment)

Heapq (priority queue for A*)

IPython Display (for animation effect)

The environment is dynamic, meaning obstacles move during execution, making path execution non-trivial.

3️⃣ Algorithm Used — A* Pathfinding

The A* algorithm is used to calculate the shortest, least-cost path through the grid.

Key Features of the A* in This Project

Uses Manhattan distance as the heuristic

Avoids:

Roadblocks

Cells with moving cars

High-cost traffic (minimizes overall travel cost)

Uses a priority queue to explore the best possible next step

Reconstructs the final path from start to goal

The system first computes an initial path, then simulates movement step-by-step along that path.

Dynamic Component

During execution:

Moving cars may block the path

If a collision occurs, the simulation stops

The environment updates visually after every step

This makes the navigation feel realistic and challenging.

4️⃣ Results
✔️ Path Found Successfully

The program generates:

A valid starting point

A valid goal

An optimal route calculated by the A* algorithm

✔️ Real-Time Simulation

As the agent moves along the path:

Each step is visualized

Moving cars shift positions

Possible outcomes:

Goal Reached (successful navigation)

Path Blocked by a moving car

✔️ Visualization

The simulation shows:

Grid layout

Path drawn in black

Start and goal markers

Static traffic zones

Roadblocks

Moving cars

A dynamic visual update occurs every 0.5 seconds, creating an animation of the navigation process.

5️⃣ How to Run the Project
Step 1 — Install Dependencies
pip install numpy matplotlib


(If using Jupyter Notebook, no extra steps are needed.)

Step 2 — Save the Script

Save the entire code in:

autonomous_navigation_dynamic_grid.py

Step 3 — Run the Program
python autonomous_navigation_dynamic_grid.py

Step 4 — View the Simulation

The program will:

Generate a grid

Select start & goal automatically

Compute a path

Begin animated navigation

Watch the updates as the autonomous agent moves step-by-step through the environment.

6️⃣ Developer’s Role

The developer is responsible for:

Designing the dynamic grid environment

Creating cost-based cell behavior

Implementing A* pathfinding

Integrating moving obstacle logic

Building real-time animation using Matplotlib

Handling collision detection and termination conditions

Structuring code into clean, understandable functions

The project showcases skills in:

Search algorithms

Dynamic simulations

Path planning

Visualization in Python

Handling real-time updates in grid-based environments
