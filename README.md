# Sokoban Search Algorithm

Implemented various search algorithms with python to create working solvers for the puzzle game Sokoban.

Sokoban can be played online at this link: https://www.sokobanonline.com/play 

`solution.py` contains all of the heuristics and anytime algorithms. 

`search.py` contains default implementations of search algorithms discussed in class.

`sokoban.py` specifies the search to the Sokoban domain, specifically. This file also contains testing problems with string representations. 

`autograder.py` contains test cases. 

- - - -

### Implementation Highlights

* Implemented a Manhattan distance heuristic (heur_manhattan_distance(state)). This heuristic will be used to estimate how many moves a current state is from a goal state. The Manhattan distance between coordinates (x0,y0) and (x1,y1) is | x0 − x1 | + | y0 − y1 | . Implementation calculates the sum of Manhattan distances between each box that has yet to be stored and the storage point nearest to it. Ignore the positions of obstacles in your calculations and assume that many boxes can be stored at one location. 
* Implemented a non-trivial heuristic `heur_alternate(state)` for Sokoban that improves on the Manhattan distance heuristic.
* Implemented three alternative f-value functions `fval_function(sNode, weight)`, `fval_function_XUP(sN,weight)`, and `fval_function_XDP(sN,weight))` to create variations of A* (Weighted A*, Weighted A* (XUP) and Weighted A* (XDP)).
* Implemented Anytime Weighted A* `anytime_weighted_astar(initial_state, heur_fn, weight, timebound)`. This will be an iterative form of Weighted A* search that can run within a fixed time bound. 
* Implemented Anytime Greedy Best-First Search `anytime_gbfs(initial_state, heur_fn, timebound)`. This is another iterative search that can run within a fixed time bound. 

- - - -
