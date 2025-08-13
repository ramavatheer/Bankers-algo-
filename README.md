# Banker's Algorithm Visualizer

A modern, interactive web application that visualizes the Banker's Algorithm for deadlock avoidance in operating systems. This tool helps students and professionals understand how the algorithm works through dynamic visual representation and step-by-step execution.

## Getting Started


## Input Format

### System Configuration
- **Number of Processes**: Integer (e.g., 5)
- **Number of Resources**: Integer (e.g., 3)
- **Total Resources**: Comma-separated values (e.g., `10,5,7`)

### Matrix Input Format
Matrices are entered as semicolon-separated rows with comma-separated values:

```
Row1: value1,value2,value3
Row2: value1,value2,value3
Format: value1,value2,value3;value1,value2,value3;value1,value2,value3
```

### Example Input
```
Processes: 5
Resources: 3
Total Resources: 10,5,7
Allocation Matrix: 0,1,0;2,0,0;3,0,2;2,1,1;0,0,2
Max Matrix: 7,5,3;3,2,2;9,0,2;4,2,2;5,3,3
```

##  Test Cases

### Test Case 1: Safe System (Default)
```
Processes: 5
Resources: 3
Total Resources: [10, 5, 7]

Allocation Matrix:
P0: [0, 1, 0]
P1: [2, 0, 0]
P2: [3, 0, 2]
P3: [2, 1, 1]
P4: [0, 0, 2]

Max Matrix:
P0: [7, 5, 3]
P1: [3, 2, 2]
P2: [9, 0, 2]
P3: [4, 2, 2]
P4: [5, 3, 3]

Expected Result: SAFE - Sequence: P1 → P3 → P4 → P0 → P2
```

### Test Case 2: Unsafe System
```
Processes: 5
Resources: 3
Total Resources: [10, 5, 7]

Allocation Matrix: 0,1,0;2,0,0;3,0,2;2,1,1;0,0,2
Max Matrix: 8,5,3;3,2,2;9,0,2;4,2,2;5,3,3

Expected Result: UNSAFE - No safe sequence exists
```

### Test Case 3: Minimal Safe System
```
Processes: 3
Resources: 2
Total Resources: [5, 3]

Allocation Matrix: 1,0;1,1;0,1
Max Matrix: 3,2;2,1;1,2

Expected Result: SAFE
```

## Algorithm Details

### Banker's Algorithm Steps
1. **Initialize** work vector with available resources
2. **Find Process** that can be satisfied with current available resources
3. **Allocate Resources** to the found process
4. **Release Resources** when process completes
5. **Repeat** until all processes are completed or no safe process is found

### Safety Algorithm
```javascript
function isSafe(processes, available, maxMatrix, allocationMatrix) {
    // Calculate Need Matrix = Max - Allocation
    // Initialize finish array and work vector
    // Find processes that can complete
    // Return safe sequence or indicate unsafe state
}
```

