# DAA-EX-8
# Travelling Salesman Problem using Branch and Bound

## Overview

This project solves the Travelling Salesman Problem (TSP) using the Branch and Bound technique. A lower-bound estimation based on reduced cost matrices is used to efficiently eliminate non-promising branches and determine the optimal Hamiltonian cycle.

## Problem Statement

Given a 5-city TSP with a known cost matrix, find the minimum cost Hamiltonian cycle using Branch and Bound with a lower-bound estimation based on reduced cost matrices.

The program displays:

* The cost matrix.
* The optimal tour.
* The total minimum cost.
* The Branch and Bound result.

## Cost Matrix

The cities are represented as `0, 1, 2, 3, 4`.

| From / To |  0 |  1 |  2 |  3 |  4 |
| --------- | -: | -: | -: | -: | -: |
| **0**     |  0 | 20 | 30 | 10 | 11 |
| **1**     | 15 |  0 | 16 |  4 |  2 |
| **2**     |  3 |  5 |  0 |  2 |  4 |
| **3**     | 19 |  6 | 18 |  0 |  3 |
| **4**     | 16 |  4 |  7 | 16 |  0 |

## Objectives

* Implement the Travelling Salesman Problem.
* Apply Branch and Bound.
* Calculate lower bounds using matrix reduction.
* Prune non-promising branches.
* Find the optimal Hamiltonian cycle.
* Calculate the minimum total cost.

## Branch and Bound Technique

The algorithm works by maintaining partial tours and calculating a lower bound for each branch.

### Steps

1. Start with the complete cost matrix.
2. Perform row reduction.
3. Perform column reduction.
4. Calculate the reduction cost.
5. Select a possible next city.
6. Create a reduced child matrix.
7. Calculate the lower bound of the child.
8. Discard the child if its bound is greater than the current best cost.
9. Continue until all cities are included in a complete tour.

## Lower Bound Estimation

The lower bound is calculated using the cost of the current partial path and the reduction cost of the remaining matrix.

```text
Lower Bound =
Current Cost + Matrix Reduction Cost
```

Matrix reduction helps estimate the minimum possible cost required to complete a partial tour.

## Optimal Tour

The optimal Hamiltonian cycle for the given matrix is:

```text
0 → 3 → 1 → 4 → 2 → 0
```

## Cost Calculation

```text
0 → 3 = 10
3 → 1 = 6
1 → 4 = 2
4 → 2 = 7
2 → 0 = 3
```

Therefore:

```text
Total Cost = 10 + 6 + 2 + 7 + 3
           = 28
```

### Final Result

**Optimal Tour:**

```text
0 → 3 → 1 → 4 → 2 → 0
```

**Minimum Cost: 28**

## Complexity Analysis

| Parameter        | Complexity |
| ---------------- | ---------- |
| Worst-Case Time  | O(N!)      |
| Space Complexity | O(N²)      |

The TSP has factorial search complexity in the worst case. Branch and Bound improves practical performance by pruning branches that cannot produce a better solution.

## Sample Output

```text
TRAVELLING SALESMAN PROBLEM
BRANCH AND BOUND

Cost Matrix:

[0, 20, 30, 10, 11]
[15, 0, 16, 4, 2]
[3, 5, 0, 2, 4]
[19, 6, 18, 0, 3]
[16, 4, 7, 16, 0]

Optimal Tour:
0 -> 3 -> 1 -> 4 -> 2 -> 0

Minimum Cost: 28

Optimal Hamiltonian Cycle Found Successfully.
```

## Project Structure

```text
TSP-Branch-and-Bound/
│
├── tsp_branch_bound.py
├── index.html
└── README.md
```

## Applications

* Route Optimization
* Delivery Route Planning
* Logistics
* Vehicle Routing
* Network Optimization
* Scheduling
* Transportation Planning

## Advantages

* Reduces the search space through pruning.
* Provides an exact optimal solution.
* Uses matrix reduction to obtain useful lower bounds.
* Suitable for small and medium-sized TSP instances.

## Limitations

* Worst-case time complexity is factorial.
* Performance decreases significantly as the number of cities increases.
* Requires more computation than heuristic approaches for large instances.

## Technologies Used

* Python 3
* Branch and Bound
* Matrix Reduction
* Graph Theory
* Combinatorial Optimization

## Conclusion

The Branch and Bound approach successfully determines the optimal Hamiltonian cycle for the given 5-city TSP. By using reduced cost matrices to calculate lower bounds, non-promising branches can be pruned, reducing unnecessary exploration.

For the given cost matrix, the optimal tour is:

```text
0 → 3 → 1 → 4 → 2 → 0
```

with a minimum total cost of **28**.

## Author

**Akash N**

B.E. Computer Science and Engineering (AI)
Chennai Institute of Technology
