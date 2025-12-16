Algorithm: BFS(Graph, Start)
1.  create an empty queue Q
2.  create an empty set VISITED
3.  mark Start as visited
4.  enqueue Start into Q
5.  while Q is not empty do
6.      node ← dequeue Q
7.      visit node
8.      
9.      for each neighbor N of node do
10.         if N is not visited then
11.             mark N as visited
12.             enqueue N into Q
13.         end if
14.     end for
15. end while
