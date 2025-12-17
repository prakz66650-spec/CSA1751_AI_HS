## 1. Breadth First Search (BFS)

```
BFS(Graph, StartNode)
    // Graph is represented as adjacency list
    CREATE empty queue Q
    CREATE empty set Visited

    ADD StartNode to Visited
    ENQUEUE StartNode into Q

    WHILE Q is not empty DO
        CurrentNode ← DEQUEUE Q
        VISIT CurrentNode

        FOR each Neighbor of CurrentNode in Graph DO
            IF Neighbor not in Visited THEN
                ADD Neighbor to Visited
                ENQUEUE Neighbor into Q
            END IF
        END FOR
    END WHILE
END BFS
```


## 3. Water Jug Problem (State Space Representation)

```
WaterJugSolver(JugA, JugB, Target)
    CREATE empty queue Q
    CREATE empty set Visited

    InitialState ← (JugA_full, JugB_empty)
    ENQUEUE InitialState into Q
    ADD InitialState to Visited

    WHILE Q is not empty DO
        (A, B) ← DEQUEUE Q

        IF A = Target OR B = Target THEN
            PRINT Solution
            RETURN
        END IF

        FOR each PossibleNextState from (A, B) DO
            IF PossibleNextState not in Visited THEN
                ADD PossibleNextState to Visited
                ENQUEUE PossibleNextState into Q
            END IF
        END FOR
    END WHILE
END WaterJugSolver
```


## 4. General Constraint Satisfaction Problem (CSP)

```
CSP_Backtracking(Assignment)
    IF Assignment is complete THEN
        RETURN Assignment
    END IF

    Variable ← SELECT unassigned variable

    FOR each Value in Domain(Variable) DO
        IF Value is consistent with Assignment THEN
            ASSIGN Variable ← Value

            Result ← CSP_Backtracking(Assignment)
            IF Result ≠ FAILURE THEN
                RETURN Result
            END IF

            REMOVE assignment of Variable
        END IF
    END FOR

    RETURN FAILURE
END CSP_Backtracking
```
---

**Author:** *Dr.M.Prakash*
**Course / Project:** *Optional*
**Last Updated:** *DD-MM-YYYY*
