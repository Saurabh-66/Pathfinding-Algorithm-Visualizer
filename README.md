# Pathfinding-Algorithm-Visualizer
Pathfinding algorithms are an effective way to find the most optimal or shortest path between the source node and the destination node in a graph (it can be directed or undirected, weighted or unweighted graph). We are going to visually see the internal functioning of 3 pathfinding algorithms, i.e. ***Breadth first search (BFS)***, **Dijkstra algorithm** and **A* search algorithm** and conclude which technique is best to use under different circumstances. The visualizer is built using **Pygame** which is a **Python** module.

## Table of Contents

- [Breadth First Search (BFS)](#breadth-first-search-bfs)
- [Dijkstra](#dijkstra)
- [A* Search](#a-search)
- [Dijkstra vs A* Search](#dijkstra-vs-a-search)
- [Conclusion](#conclusion)

### Breadth First Search (BFS)

Breadth first search is used to find shortest path when the cost of all edges is equal (let say 1). Here a queue is used to keep the track of nodes which are to be processed, the nodes which would be processed after that are its neighbors. Below is the visual representation of BFS (blue rectangle is the source vertex, green rectangles are the nodes which are processed, white rectangles represent the shortest path between source and target vertex, orange rectangles represent obstacles and pink node represents the target vertex).

![BFS](https://github.com/Saurabh-66/Pathfinding-Algorithm-Visualizer/blob/master/photos/bfs_1.gif)

In the above BFS simulation, the movements allowed are up, down, left and right and the node which we are visiting next shouldn't be outside the grid or shouldn't be an obstacle.

Below is a more user driven visualization where the user selects the target node and gets the shortest path between source and target vertex along with the nodes explored (while performing the BFS).

![BFS](https://github.com/Saurabh-66/Pathfinding-Algorithm-Visualizer/blob/master/photos/bfs_2.gif)

### Dijkstra

Dijkstra algorithm is used to find the shortest path from a single source to all nodes in a weighted graph with non-negative edge weights. Here a min-heap is used (it's implemented using priority_queue in C++ or heapq module in Python) and the distance to reach a particular node is updated if and only if the distance via the new route is less than the current distance to reach the node. Below is the weighted graph used to demonstrate the visualization of dijkstra algorithm.

![Dijkstra](https://github.com/Saurabh-66/Pathfinding-Algorithm-Visualizer/blob/master/photos/dijkstra_1.gif)

Simulation of dijkstra algorithm is demonstrated below (blue dot is the source vertex, purple vertex is the target vertex, red dot shows the path and pink vertex shows the current vertex which is being processed).

![Dijkstra](https://github.com/Saurabh-66/Pathfinding-Algorithm-Visualizer/blob/master/photos/dijkstra_2.gif)

### A* Search

A* search algorithm is similar to that of dijkstra algorithm, it uses a heuristic function to decide which node to process next. Here the manhattan distance (sum of horizontal and vertical distances between the points in a grid) is used as the heuristic function.

![A* Search](https://github.com/Saurabh-66/Pathfinding-Algorithm-Visualizer/blob/master/photos/asearch_1.gif)

### Dijkstra vs A* Search

The simulation of dijkstra and A* search shows that if we have a fixed source and target node, the A* search algorithm finds the shortest path much faster than the dijkstra algorithm.

![Dijkstra vs A* Search](https://github.com/Saurabh-66/Pathfinding-Algorithm-Visualizer/blob/master/photos/dijkasearch_1.gif)

### Conclusion

We saw the inner functioning of all the 3 pathfinding algorithms using visual representation. Each of the algorithm as its own merits and demerits and can be used depending on the use case. For eg. if we need to find the shortest path between source and vertex and all edge weights are same then we can use breadth first search. If the graph is weighted (non-negative weights) and we need to find shortest distance to all nodes from the source node then dijkstra algorithm can be used and if the source and target vertex are fixed and we need to find the shortest path then we can apply heuristic function and modify the dijkstra algorithm to reach the possible path much faster and this technique is the A* search algorithm (the only drawback here is you will get shortest path between source and target vertex but if the goal is to find shortest path to all nodes from source then dijkstra algorithm is more prefereable).
