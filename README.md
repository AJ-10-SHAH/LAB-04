# LAB-04
A* Implementation
This code implements the A* search algorithm to find the shortest path between two cities in a graph. The graph is represented using a dictionary where each key is a city and the value is another dictionary containing the neighboring cities and the distance between them.

The Node class represents a node in the graph and stores the following information: the name of the node, a reference to its parent node (used to reconstruct the path), the distance from the start node (denoted by g), the heuristic distance to the goal node (denoted by h), and the total cost (denoted by f = g + h). The Graph class represents the graph and provides methods to add edges, get neighbors, and get all nodes in the graph. The a_star_search function implements the A* search algorithm using the Graph class and the Node class.

The algorithm works as follows:

Initialize the open list with the start node.
While the open list is not empty, select the node with the lowest f value and remove it from the open list.
If the selected node is the goal node, the path has been found. Trace back from the goal node to the start node using the parent references and return the path.
Otherwise, expand the node by generating its neighboring nodes and calculating their g, h, and f values. If a neighboring node is already on the open list, update its values if the new values are better. If a neighboring node is not on the open list, add it to the open list.
The heuristic function used in this implementation is the straight-line distance between two cities (also known as the Euclidean distance) which is stored in the heuristics dictionary. The getNode function in the Graph class is used to create a Node object for a given city and its heuristic distance to the goal node.

The main function creates the graph and runs the A* search algorithm to find the shortest path between two cities. The path is printed to the console.
