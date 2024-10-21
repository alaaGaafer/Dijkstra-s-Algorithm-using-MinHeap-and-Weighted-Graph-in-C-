# Dijkstra's Algorithm using MinHeap and Weighted Graph in C++

## Overview

This program implements **Dijkstra's Shortest Path Algorithm** using a **MinHeap** and a **Weighted Graph**. The program reads a graph from a file (`graph.txt`) and finds the shortest path from a starting node to all other nodes in the graph.

## Features

- Load a weighted graph from a text file.
- Implement Dijkstra's algorithm to calculate the shortest path from a given start node to all other nodes in the graph.
- Display the result, including the cost to reach each node and the previous node in the shortest path.

## How it Works

1. **Graph Representation**: 
   - The graph is represented using an adjacency list or matrix (implementation details can be found in `WeightedGraph.h`).

2. **MinHeap**:
   - A priority queue is used to always process the next closest node (minimum cost). The heap structure helps efficiently extract the minimum and update distances.

3. **Dijkstra’s Algorithm**:
   - The algorithm calculates the shortest path from a given source node (`g` in this case) to all other nodes in the graph. It prints the cost to reach each node and the previous node for the shortest path.

## Input Format

The program expects the graph data to be provided in a file called `graph.txt`. Each line in the file should represent an edge between two nodes and its corresponding weight.

Example format for `graph.txt`:
```
A B 4
A C 2
B C 1
B D 5
C D 8
C E 10
D E 2
```

This represents a weighted graph with edges and their corresponding weights between nodes.


## Example Output

```
Graph Loaded:
A -> B (4)
A -> C (2)
B -> C (1)
B -> D (5)
C -> D (8)
C -> E (10)
D -> E (2)

Node    Cost    Previous
A       0       -
B       4       A
C       2       A
D       9       B
E       11      D
```

## File Structure

- `main.cpp`: Contains the main logic to load the graph, run Dijkstra’s algorithm, and display the results.
- `MinHeap.h`: Implements the MinHeap data structure used for priority queue operations.
- `WeightedGraph.h`: Implements the weighted graph structure and the Dijkstra's algorithm.

