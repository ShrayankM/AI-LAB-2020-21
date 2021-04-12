# Informed Search Algorithms

## Programs
1. Best-First-Search (Shortest path)
2. A* Search Algorithm (Shortest path)

## Best-First-Search Program:
  * Heuristic used is Euclidean distance between 2 nodes.
  * As best first search uses Greedy Approach and selects the current best solution no guarantee of finding optimal solution.
  * f(n) = h(n)
  * h(n) is euclidean distance from node (n) to goal.

## A* Search Algorithm:
  * Heuristic used is Euclidean distance between 2 nodes.
  * As A* search uses heuristic and cost to get to current node we will get a optimal solution.
  * f(n) = g(n) + h(n).
  * h(n) is euclidean distance from node (n) to goal.
  * g(n) is cost from source to current node (n).

## Description:
  * Every node in graph has co-ordinates (x, y) to calculate heuristic, defined using class Node.
  * Graph DS is used to add Nodes as vertices, edges and the cost between 2 nodes defined using class Graph.
  * Open list is used to keep track of Nodes yet to be explored and Closed List is used to keep track of nodes that are done.


## Input
   * Graph DS: 
```bash
    g = Graph(len(nodes))
    g.add_edge('1', '2', 3)
    g.add_edge('1', '3', 4)
    g.add_edge('1', '4', 2)
    g.add_edge('3', '5', 2)
    g.add_edge('3', '6', 5)
    g.add_edge('4', '6', 6)
    g.add_edge('5', '7', 6)
    g.add_edge('6', '7', 3)
    g.add_edge('7', '8', 4)
```

## Output (Best-First-Search)
   * In output for every node selected the neighbouring heuristics are shown.
```bash
    For Node = 1
    2 5.0
    3 2.8284271247461903
    4 4.123105625617661
    For Node = 3
    5 3.1622776601683795
    6 2.0
    For Node = 6
    4 4.123105625617661
    7 2.0
    For Node = 7
    5 3.1622776601683795
    8 0.0
    Destination Reached
    1 --> 3 --> 6 --> 7 --> 8
    Cost = 16
```

## Output (A* Search Algorithm)
   * In output for every node selected the neighbouring heuristics are shown.
```bash
    For Node = 1
    2 8.0 1
    3 6.82842712474619 1
    4 6.123105625617661 1
    For Node = 4
    6 10.0 4
    For Node = 3
    5 9.16227766016838 3
    For Node = 2
    For Node = 5
    7 14.0 5
    For Node = 6
    7 13.0 6
    For Node = 7
    8 15.0 7
    Destination Reached
    8 --> 7 --> 6 --> 4 --> 1
    Cost = 15.0
```

## Conclusion: 
   * Best-first search gives sub-optimal result and A* gives optimal result for the same graph as seen in the output above.