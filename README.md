# 🚗💡 Autonomous Vehicle Route Planning (with Moving Traffic!)

This project is a fun simulation that shows how an autonomous car might find its way through a busy grid full of **traffic**, **roadblocks**, and **moving cars** — all while using the A* pathfinding algorithm to choose the best possible route.

The map updates in real time, cars move randomly, and the vehicle tries to reach its goal without crashing. If something blocks the way, the simulation reacts immediately!

---

## 🌍 What This Simulation Does

- Generates a **20×20 grid** that represents a small city map.
- Some cells are:
  - 🟧 *Static traffic* — still drivable, but slow  
  - ⛔ *Roadblocks* — completely impossible to drive through  
  - 🟦 *Moving cars* — obstacles that change every step  
- Your autonomous car:
  - Picks a random starting point
  - Aims for a random goal
  - Uses **A\*** to find the best path
  - Moves one step at a time toward the goal  
- You get a live animation showing:
  - The grid  
  - The computed path  
  - Moving cars  
  - The vehicle’s current position  

If the car gets blocked by another moving car, the simulation tells you. If it reaches its destination — success! 🎉

---

## 🧠 Behind the Scenes

Here’s what powers the system:

### ✔️ A* Pathfinding  
The car uses the A* algorithm, which balances:
- Actual distance traveled (`g`)
- Estimated distance remaining (`h`, using Manhattan distance)

### ✔️ Dynamic Traffic  
Each step:
- Moving cars change their positions randomly.
- The autonomous car checks if the next cell is blocked.
- Everything is redrawn smoothly.

### ✔️ Grid Layout  
Every cell has a cost:
- Normal road = `1`
- Static traffic = `5` (slows down the path)
- Roadblock = `-1` (never allowed)

This makes the pathfinding feel realistic.
