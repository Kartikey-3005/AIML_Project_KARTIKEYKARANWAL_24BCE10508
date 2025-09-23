# Autonomous Delivery Agent
This project implements an autonomous delivery agent that navigates a 2D grid city to deliver packages efficiently. The agent is designed to be rational, choosing actions that maximize delivery efficiency while considering constraints like time and fuel (represented as terrain costs). Artificial IntAnelligence and Machine Learning project developed by Kartikey Karanwal.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-None-lightgrey)
![Stars](https://img.shields.io/github/stars/Kartikey-3005/AIML_Project_KARTIKEYKARANWAL_24BCE10508?style=social)
![Forks](https://img.shields.io/github/forks/Kartikey-3005/AIML_Project_KARTIKEYKARANWAL_24BCE10508?style=social)
<img width="344" height="331" alt="Screenshot 2025-09-23 215735" src="https://github.com/user-attachments/assets/d1b7194d-4505-4a8d-a0ff-bede526658b4" />


##  Features

*  Environment Modeling: The agent can navigate environments with static obstacles, varying terrain costs, and dynamic moving obstacles.

* Pathfinding Algorithms:

    * Uninformed Search:

        * Breadth-First Search (BFS)

        * Uniform-Cost Search (UCS)

    * Informed Search:

        * A* Search with the Manhattan distance heuristic.

    * Dynamic Replanning:

        * A simulation mode where the agent uses A* to replan its path at each time step   to      avoid dynamic obstacles.

* Experimental Comparison: The project allows for comparing the performance of these algorithms based on path cost, nodes expanded, and execution time.

## 📁 Project Structure
```
├── maps/
│   ├── small.txt
│   ├── medium.txt
│   ├── large.txt
│   └── dynamic.txt
├── algorithms.py
├── environment.py
├── main.py
├── utils.py
├── README.md
└── report.md
```

## 🚀 Quick Start

### Prerequisites

* Python 3.x

### Instructions

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/autonomous-delivery-agent.git](https://github.com/your-username/autonomous-delivery-agent.git)
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd autonomous-delivery-agent
    ```

3.  **Run the application:**
    ```bash
    python main.py
    ```

Upon running the script, you will be presented with a menu to select a map and an algorithm to execute.

---
## Map File Format

The map files (`.txt`) have a simple format:

* The grid is represented by characters:
    * `S`: Start position
    * `G`: Goal position
    * `.`: Standard terrain (cost = 1)
    * `1`-`9`: Varied terrain with corresponding movement cost.
    * `X`: Static obstacle (wall).
* Dynamic obstacles are defined after a `---` separator. Each line represents an obstacle's position and the time steps at which it appears:
    * `obstacle_id,row,col,time1,time2,...`


