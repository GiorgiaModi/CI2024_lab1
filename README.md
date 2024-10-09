### Set cover problem
Given a family of sets, find the subfamily of minimum cost that covers all elements in the universe. Several possible greedy algorithms.

## Lab 1 text
Solve efficiently these instances customizing a technique discussed in class
<img width="600" alt="Screenshot 2024-10-09 alle 17 31 00" src="https://github.com/user-attachments/assets/6ddcee7e-1d36-4e8a-ac4b-db7c775eb993">

## Implemented Solutions

I have reported professor's solutions and I have implemented two optimization algorithms to solve the given problem:

- **Solution 1** is based on **Simulated Annealing**
- **Solution 2** is based on **Tabu Search**

### Results

| Instance | Universe Size | Num Sets | Density | Execution Time Sol 1 | Execution Time Sol 2 | Fitness Solution 1 | Fitness Solution 2 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | 100 | 10 | 0.2 | 0.1s | 0.6s | -**301**.7654322960134 | -**283**.5373559355688 |
| 2 | 1,000 | 100 | 0.2 | 0.1s | 1.6s | -**7105**.292537437867 | -**6045**.412482547696 |
| 3 | 10,000 | 1,000 | 0.2 | 1.1s | 16.2s | -**359025**.4417471046 | -**194453**.43020167478 |
| 4 | 100,000 | 10,000 | 0.1 | 3m 45.1s | 81m 32.1s | -**105543124**.2185235 | -**15939984**.115404114 |
| 5 | 100,000 | 10,000 | 0.2 | 3m 56.6s | 82m 6.8s | -**231371537**.8134606 | -**34334262**.06071715 |
| 6 | 100,000 | 10,000 | 0.3 | 3m 49.9s | 87m 5.3s | -**347324626**.9237651 | -**56080103**.33176648 |


Based on the performance data in the table:

1. **Execution Time:** **Simulated Annealing (Solution 1)** is consistently faster than **Tabu Search (Solution 2)** across all instances. For smaller instances (Instance 1 and 2), the difference in execution time is relatively small, but as the problem size increases (e.g., Instance 4 and above), Tabu Search becomes significantly slower, with a runtime exceeding one hour on the largest instances.

2. **Fitness:** **Tabu Search (Solution 2)** produces better fitness values across all instances, indicating that while it is slower, it tends to find better solutions. 

While Simulated Annealing handles larger instances more efficiently in terms of execution time, the trade-off is a lower fitness quality. Tabu Search, though computationally expensive, proves to be more robust in terms of solution quality, especially for larger and more complex instances.

The code I've uploaded is only for instance 2, but I've tested all the instances and reported the results in the table and in the folder "plots".
