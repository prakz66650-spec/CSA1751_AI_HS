Breadth First Search (BFS) – Pseudocode

Algorithm: BFS(Graph, Start)

Create an empty queue Q

Create an empty set VISITED

Mark Start as visited

Enqueue Start into Q

While Q is not empty,\n do
 Dequeue an element from Q and store it in node
7. Visit node
8. For each neighbor N of node, do

If N is not visited, then

Mark N as visited

Enqueue N into Q
