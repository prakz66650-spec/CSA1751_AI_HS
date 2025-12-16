*Algorithm for BFS Traversal*


BFS(graph, start):
    create an empty queue
    mark start as visited
    enqueue start

    while queue is not empty:
        node = dequeue
        visit node
        for each neighbor of node:
            if neighbor is not visited:
                mark visited
                enqueue neighbor
