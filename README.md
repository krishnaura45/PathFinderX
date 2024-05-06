<h1 align="center">PathFinderX: Path Planning with Bidirectional A* Algorithm</h1>

### INTRODUCTION<hr>

<img align="right" src='https://github.com/krishnaura45/PathFinderX/assets/118080140/8cc32d0f-66ff-4909-842e-e0429832d86a' height=280>

- **Path planning** is crucial in **robotics** for **safe navigation**. It involves finding the best route from a start to a goal while avoiding obstacles.
- Bidirectional A*
  - A pathfinding algorithm widely used in robotics for **efficient** path planning.
  - **simultaneously explores** from start and goal nodes to find the shortest path efficiently.
  - offers advantages such as **reduced computational complexity** and **guaranteed optimality**.
- This project **aims to implement** and assess Bidirectional A* for robotic path planning, focusing on efficiency and optimality.<br>

### RELATED WORKS / ALGORITHMS<hr>
<img align="center" src='https://github.com/krishnaura45/PathFinderX/assets/118080140/ec7f3d0d-d7bb-4f20-bed2-7b20fe8dca2e' width=740>
<img align="center" src='https://github.com/krishnaura45/PathFinderX/assets/118080140/6ba76f8c-ce62-43f0-b233-20e4676031f5' width=740>

### PROBLEM STATEMENT<hr>
- **Autonomous robots require efficient path planning** to navigate obstacles and reach goals.
- **Existing Solutions**: Traditional path planning algorithms like A* are effective but may suffer from high computational complexity, especially in large search spaces.
- **Need for Improvement**: There is a need for more efficient path planning algorithms that can handle large-scale environments and complex robotic systems without sacrificing optimality.
- This project aims to address this challenge by implementing the Bidirectional A* algorithm for robotic path planning.
- The project will **explore the effectiveness of Bidirectional A*** in various robotic applications, considering factors such as algorithmic performance, computational resources, and real-world applicability.


### OBJECTIVES<hr>
- Explore path planning algorithms, especially A* algorithm.
- Develop a robust implementation of the Bidirectional A* algorithm for efficient path planning in robotics.
- Assess efficiency, optimality, and scalability compared to traditional algorithms.
- Showcase practical benefits in real-world robotic navigation scenarios.

### IMPLEMENTATION<HR>
#### Exploration - A* Algorithm
<img align="right" src='https://github.com/zhm-real/path-planning-algorithms/blob/master/Search_based_Planning/gif/Astar.gif' height=240>

- A* algorithm is a popular heuristic search based algorithm used for pathfinding and optimization in graphical environments or grids.
- It efficiently finds the shortest path from a start to a goal position in a graph (or grid) by combining Dijkstra's algorithm with heuristics.
- It relies on a heuristic function (e.g., Manhattan distance) to estimate the cost to reach the goal from each node.
- It guarantees finding the optimal path if certain conditions are met and is complete if a solution exists.
- Limitations:
  - The algorithm may consume significant memory, particularly in large graphs.
  - Effectiveness depends on the quality of the heuristic function. Inaccurate or poorly chosen heuristics can lead to suboptimal paths or inefficient search behavior.

#### Overview - Bidirectional A* Algorithm
<img align="right" src='https://github.com/zhm-real/path-planning-algorithms/blob/master/Search_based_Planning/gif/Bi-Astar.gif' height=240>

- Bidirectional A* is a variant of the A* algorithm used for path planning. It explores paths simultaneously from both the start and goal nodes towards each other.
- Operation: Two search trees are maintained, one from the start node and one from the goal node. Nodes are expanded from both trees based on their heuristic estimates, with the goal of meeting in the middle to find the optimal path.
- It reduces the search space by exploring from both ends simultaneously, resulting in faster convergence towards the optimal path compared to traditional A*.
- Considerations:
  - While Bidirectional A* offers advantages in terms of efficiency, it may require careful synchronization between the two search trees to ensure correct operation.
  - Heuristic quality and selection can significantly impact the algorithm's performance and effectiveness in finding the optimal path.

#### Pseudo code - Bidirectional A* Algorithm
<img align="center" src='https://github.com/krishnaura45/PathFinderX/assets/118080140/c1c93341-e550-4a03-83ab-25acebd98728' width=720><br>

<img align="center" src='https://github.com/krishnaura45/PathFinderX/assets/118080140/d5eaf28c-f737-4862-a2a2-4ef2206baea4' width=300>

####  Advantages - Bidirectional A* Algorithm
- Efficiency: Bidirectional A* explores paths from both the start and goal nodes simultaneously, significantly reducing the search space and computational complexity compared to traditional A*.
- Faster Convergence: By converging towards each other, the algorithm tends to find the optimal path more quickly, especially in large and complex environments, leading to faster navigation times.
- Optimality Guarantee: It maintains the optimality of A* while offering improved efficiency, ensuring that the shortest path is found from the start to the goal node.
- Scalability: The algorithm's ability to divide the search process into two independent sub-problems makes it well-suited for large-scale environments and complex robotic systems, enhancing scalability and performance.
- Reduction in Memory Usage: It requires maintaining two separate search trees, which may reduce memory usage compared to traditional A* when searching in large graphs or environments.


### RESULTS<hr>
<img align="right" src='https://github.com/krishnaura45/PathFinderX/assets/118080140/089a5459-453d-4d67-a8e9-9010e2a54d70' height=240>

- The section alongside provides a visual representation of the obstacle map's final configuration, which consists of:
  - **Start Node**: The initial position from which the robot begins its journey towards the goal. [10,10]
  - **Goal Node**: The desired destination that the robot aims to reach. [50,50]
  - **Optimal Path**
  - **Meeting Point**: The point where the paths explored from the start and goal nodes converge. This point signifies the successful completion of the path planning process by Bidirectional A*, as it indicates the discovery of an optimal path connecting the start and goal nodes.


<br><img src='https://github.com/krishnaura45/PathFinderX/assets/118080140/76b95e47-a546-4d73-8f38-de181707998f'>

- The figures show initial, intermediate and final configurations when Bidirectional A* algorithm is applied on a particularly set environment. In all the images shown below (without grids), the starting point is located at (10,10) and the goal is located at (50,50) whereas the algorithm finds an optimal path and stops at location (35,35).
- In the context of path planning algorithms like Bidirectional A*, **f(n)** represents the **estimated total cost of the path** from the start node to the goal node passing through node n. The role of this function is **to guide the search algorithm** towards nodes that are both **low-cost** (according to g(n)) and **promising in terms of their proximity to the goal** (according to h(n)). Nodes with **lower f(n) values** are prioritized for exploration by the search algorithm, as they are likely to lead to **more optimal paths**.


### CONCLUSIONS<HR>
- **Superiority**: Bidirectional A* outperforms other algorithms, offering efficiency and optimality in robotic path planning.
- **Successful Implementation**: Bidirectional A* was successfully implemented after exploring A*, demonstrating its effectiveness.
- **Efficient and Optimal Results**: Our algorithm consistently delivers efficient and optimal paths, meeting real-world navigation needs.
- **Enhanced Autonomy**: Thus, it shows potential to enhance autonomy and efficiency in robotic applications, improving navigation capabilities.


### REFERENCES<hr>
1) Pradhan, Rahul, Kartik Agrawal, and Anubhav Nag. "Analyzing Evolution of the Olympics by Exploratory Data Analysis using R." IOP Conference Series: Materials Science and Engineering. Vol. 1099. No. 1. IOP Publishing
2) Mingyu Li. et al. Direction constraints adaptive extended bidirectional A* algorithm based on random two-dimensional map environments (2023). Retrieved from https://www.sciencedirect.com/science/article/abs/pii/S0921889023000696
3) Sánchez-Ibáñez J.R. et al. Path planning for autonomous mobile robots: A review Sensors (2021).
https://en.wikipedia.org/wiki/Bidirectional_search
4) Atsushi Sakai (2018). Python Robotics [Computer software]. Retrieved from https://arxiv.org/abs/1808.10703
5) Huiming Zhou (2020). Path Planning [Computer software]. Retrieved from https://github.com/zhm-real/PathPlanning

