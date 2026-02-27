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

Solves the knapsack problem by building a table of subproblem solutions. The optimal result is derived from this table, enabling efficient computation of maximum value within capacity.

### Output

Upon completion, the program prints:

```
Dynamic Programming solution: Value VALUE, Weight WEIGHT ITEM1 ITEM2 ITEM3 ...
```

Selected item indices are listed in ascending order.

### Java Implementation

- File: `DynProg.java`
- Reads the input file
- Executes the dynamic programming algorithm
- Outputs total value, total weight, and selected item indices

## Approach 2: Branch-and-Bound

Uses a tree-based search to explore partial solutions. Bounding functions are applied to prune the search space and improve efficiency.

### Output

Upon completion, the program prints:

```
Using Branch and Bound the best feasible solution found: Value <VALUE>, Weight <WEIGHT> <ITEM> <ITEM> ...
```

Selected item indices are listed in ascending order.

### Java Implementation

- File: `BandB.java`
- Reads the input file
- Executes the branch-and-bound algorithm
- Outputs total value, total weight, and selected item indices

## Testing and Results

Evaluate both algorithms using the following datasets:

- `easy.20.txt`
- `easy50.txt`
- `hard50.txt`
- `easy.200.txt`
- `hard.200.txt`

Record results in a table including:

- Best value found
- Total weight
- Execution time
- Any issues encountered (e.g., timeouts)

For Branch-and-Bound, also report whether a timeout occurred and the best solution found before termination.

### Example Results Table

| Dataset        | Algorithm           | Value | Weight | Time (s) | Status    |
|----------------|--------------------|-------|--------|----------|-----------|
| easy.20.txt    | Dynamic Programming | 100   | 50     | 0.500    | Completed |
| easy.20.txt    | Branch-and-Bound    | 100   | 50     | 1.200    | Completed |
| hard50.txt     | Dynamic Programming | 500   | 200    | 5.000    | Completed |
| hard50.txt     | Branch-and-Bound    | 500   | 200    | 120.000  | Timeout   |
| ...            | ...                | ...   | ...    | ...      | ...       |

## Deliverables

1. **Report (PDF)**
   - Brief overview of each implementation
   - Data structures used
   - Summary of algorithm design and results
   - Maximum two pages, 12 pt font, 1.2–1.4 line spacing

2. **Java Source Files**
   - `DynProg.java`
   - `BandB.java`

Both programs must include a `main` method that reads the input file from the command line, executes the algorithm, and prints the results.

### Submission

Submit the report (PDF) and both Java source files prior to the demo.

Be prepared to demonstrate and explain the output of both algorithms.

## Notes

- Ensure code is clear and well-structured.
- Cite any external references used.
- Be ready to explain algorithm design decisions and performance trade-offs.
