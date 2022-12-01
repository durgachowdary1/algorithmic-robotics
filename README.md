# algorithmic-robotics


> The planner takes advantage of a modified Weighted A* algorithm to catch moving objects in the provided environments (maps). In order to make the robot be able to take actions promptly, the algorithm uses a compressed 1D search space (cell index) instead of 3D (x, y, theta). The lower-dimensional search space provides the algorihm with higher efficiency and lower computation in finding the solution. 

> If a complete, valid path has been generated during one call to the planner function using the Weighted A*, the plan (stored in a map) can be always re-used in the following calls to the planner function. The plan will be re-computed/ updated when: 

- The robot approaches the moving object closer than a threshold (currently set at 5), OR
- The robot does not make a sufficiently large movement throughout successive steps.

> Again, this increases the computational efficiency of the method.

> Each motion primitive is intended to cost the same for a single move. The algorithm presently uses a fixed weight of 5. Based on the euclidean distance between the robot and the moving target, a simple heuristic is applied. The algorithm can successfully complete the tasks along nearly optimal paths and quickly under a variety of test cases, despite only using simple heuristics.


### Among these test cases are:

``` bash
Start     Goal
[1  1  0] [20 10 0] map3
[25 25 0] [40 40 0] map3
[25 35 0] [40 40 0] map3
[5  38 0] [40 40 0] map3
[2  28 0] [40 40 0] map3
[13 31 0] [40 40 0] map3


[70  80 0] [85 170 0] map1
[15  44 0] [167 59 0] map1
[146 72 0] [167 78 0] map1 
``` 
