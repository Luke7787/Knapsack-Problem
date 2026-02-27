# Knapsack Algorithm Analysis

This project compares two approaches to the 0-1 Knapsack Problem: Dynamic Programming and Branch-and-Bound. Both are implemented in Java and evaluated on multiple datasets to analyze runtime performance and solution quality.

## Problem Description

The 0-1 Knapsack Problem requires selecting a subset of items to maximize total value without exceeding a given capacity. Each item has an associated weight and value, and each item can either be included or excluded.

### Input Format

The input file format is as follows:

```
N
1 v1 w1
2 v2 w2
...
N vN wN
C
```

- `N` — number of items  
- Each line contains: `index value weight`  
- `C` — knapsack capacity

## Approach 1: Dynamic Programming

### Description

The Dynamic Programming (DP) approach solves the knapsack problem by building up a table of solutions to subproblems. The final solution is derived from this table, which allows for efficient computation of the optimal value and weight.

### Output

Upon termination, the program should output:
Dynamic Programming solution: Value <value>, Weight <weight> <item#> <item#> <item#> ...

The output includes the items chosen by the DP algorithm in ascending index order.

### Java Implementation

- **File Name**: `DynProg.java`
- **Main Method**: Reads the input file and runs the dynamic programming algorithm.
- **Output**: Prints the value, weight, and indices of chosen items.

## Approach 2: Branch-and-Bound

### Description

The Branch-and-Bound (B&B) approach uses a tree search to explore possible solutions. Each node represents a partial solution, with some components (items) fixed and others remaining. The algorithm uses bounding functions to prune the search tree and improve efficiency.

### Output

Upon termination, the program should output:
Using Branch and Bound the best feasible solution found: Value <value>, Weight <weight> <item> <item> <item>

The output displays the best solution found by the B&B algorithm in ascending index order.

### Java Implementation

- **File Name**: `BandB.java`
- **Main Method**: Reads the input file and runs the branch-and-bound algorithm.
- **Output**: Prints the best solution found, including value, weight, and indices of chosen items.

## Testing and Results

Run both algorithms on the following datasets to evaluate performance:

- `easy.20.txt`
- `easy50.txt`
- `hard50.txt`
- `easy.200.txt`
- `hard.200.txt`

Record the results in a table including the best value found, weight, time taken, and any issues encountered (e.g., timeouts). For Branch-and-Bound, include information on timeouts and best results up to that point.

### Example Results Table

| Dataset        | Algorithm    | Value | Weight | Time (s) | Status        |
|----------------|--------------|-------|--------|----------|---------------|
| easy.20.txt    | Dynamic Prog  | 100   | 50     | 0.5      | Completed     |
| easy.20.txt    | Branch-and-Bound | 100   | 50     | 1.2      | Completed     |
| hard50.txt     | Dynamic Prog  | 500   | 200    | 5.0      | Completed     |
| hard50.txt     | Branch-and-Bound | 500   | 200    | 120.0    | Timeout       |
| ...            | ...          | ...   | ...    | ...      | ...           |

## Deliverables

1. **Typed Report**: A typed report in PDF format documenting the basics of each implementation, data structures used, and a brief description of the algorithms. The report should be no longer than two single-sided pages, using a readable font (12 pt) with line spacing of 1.2 to 1.4.

2. **Java Files**:
   - **DynProg.java**: Contains the implementation of the Dynamic Programming algorithm.
   - **BandB.java**: Contains the implementation of the Branch-and-Bound algorithm.

Both Java files should have a `main` method that reads the input file from the command line, runs the algorithm, and outputs the results.

### Submission Instructions

Submit the following before your demo:
- **Report**: Typed and saved as a PDF.
- **Java Files**: `DynProg.java` and `BandB.java` as text files.

Ensure that you can demonstrate the outputs of both algorithms during the lab demo.

## Notes

- Ensure clarity and readability of the code.
- Document any external sources used for understanding or inspiration.
- Be prepared to explain the algorithms and their implementations during the demo.
