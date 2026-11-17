File System Representation and Search Using BFS and DFS

PROJECT DESCRIPTION
This project implements a simple file system representation using a graph data structure in C. Files and directories are represented as nodes, and the relationships between them are represented as directed edges. The program uses an adjacency matrix to store the graph and searches for a specified file using two graph traversal algorithms: Breadth-First Search (BFS) and Depth-First Search (DFS).

OBJECTIVES
To represent a file system using a graph.
To store relationships between files and directories using an adjacency matrix.
To implement Breadth-First Search (BFS) for file searching.
To implement Depth-First Search (DFS) for file searching.
To display the traversal order and search results.
TECHNOLOGIES USED
Programming Language: C
Data Structure: Graph
Graph Representation: Adjacency Matrix
Algorithms: BFS and DFS
Compiler: GCC or any standard C compiler
FEATURES
Accepts the number and names of files and directories.
Creates directed edges between parent directories and child nodes.
Displays the adjacency matrix.
Searches for a target file using BFS and DFS.
Displays the traversal order for both algorithms.
Reports whether the target file is found or not found.
Handles invalid node names in edges and invalid starting nodes.
WORKING PRINCIPLE

The user enters the number of nodes and their names.

The user enters the edges representing parent-child relationships.

The program constructs the graph using an adjacency matrix.

The adjacency matrix is displayed.

The user enters a starting node and the name of the file to search for.

BFS explores the graph level by level using a queue.

DFS explores the graph depth-wise using recursion.

The program displays the traversal order and search result for both algorithms.

ALGORITHMS USED

Breadth-First Search (BFS):

BFS visits nodes level by level, starting from the selected node. It uses a queue to manage the nodes waiting to be visited.

Depth-First Search (DFS):

DFS explores one path as deeply as possible before backtracking. This implementation uses recursion to visit nodes.

HOW TO COMPILE AND RUN
Save the program as filesystem.c.

Compile the program using GCC:

gcc filesystem.c -o filesystem

Run the program on Linux or macOS:

./filesystem

On Windows, run:

filesystem.exe

SAMPLE INPUT
Enter number of nodes (files/directories): 5 Enter the names of 5 nodes: Root Documents Images Notes Report Enter number of edges: 4 Enter 4 edges (parent child): Root Documents Root Images Documents Notes Documents Report

Enter start node: Root Enter file to search: Report

EXPECTED OUTPUT
Adjacency Matrix: 0 1 2 3 4 0 Root 0 1 1 0 0 1 Documents 0 0 0 1 1 2 Images 0 0 0 0 0 3 Notes 0 0 0 0 0 4 Report 0 0 0 0 0

--- Searching for 'Report' starting from 'Root' ---

BFS Traversal Order: Root Documents Images Notes Report BFS Result: File 'Report' FOUND

DFS Traversal Order: Root Documents Notes Report DFS Result: File 'Report' FOUND

Note: The adjacency matrix and traversal order depend on the node names, edge order, and input graph.

TIME AND SPACE COMPLEXITY
Let V represent the number of nodes and E represent the number of edges.

Finding a node by name: O(V)
Displaying the adjacency matrix: O(V^2)
BFS traversal: O(V^2)
DFS traversal: O(V^2)
Graph storage: O(V^2)
BFS and DFS take O(V^2) time in this implementation because the graph uses an adjacency matrix and scans all possible adjacent nodes for each visited node.

ADVANTAGES
Simple and easy-to-understand graph representation.
Demonstrates two important graph traversal algorithms.
Helps understand relationships between files and directories.
Provides traversal orders that can be compared.
LIMITATIONS
The program supports a maximum of 50 nodes.
Node names cannot contain spaces.
The graph must be entered manually.
Only nodes reachable from the starting node are searched.
The program represents directory relationships but does not access the actual operating system file system.
CONCLUSION
The project demonstrates how a file system can be represented as a directed graph and how files can be searched using BFS and DFS. It provides a practical understanding of graph representation, adjacency matrices, queues, recursion, and graph traversal algorithms in C.
