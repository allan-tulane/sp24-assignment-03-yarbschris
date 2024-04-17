# CMPS 2200 Assignment 3
## Answers

**Name:** Christopher Yarbro


Place all written answers from `assignment-03.md` here for easier grading.

1a) Divide $N$ by the largest currency demonimation $2^k$ to the largest whole number. The number of times $2^k$ divides into $N$ is the number of $2^k$ coins. Then, take the remainder as the new N and divide by $2^k-1$. If any $N < 2^k$ then move on to $2^k-1$. Recurse until N = 0. Sum of all counts of 2^k coins is the total number of coins


1b) For any N where $2^k$ is the highest integer for which $2^k≤N$, the greedy algorithm is the best initial step as it maximizes the reduction of $N$ in one step. Once the first denomination is selected, the problem reduces to finding change for $N−2^k$. This new problem is not dependent on the last problem and can be solved in the same way. The total solution for N combines the selected $2^k$ with the solution for $N−2^k$. Due to the binary structure of the coin denominations, using smaller coins would result in a suboptimal solution requiring more coins overall.

1c) Work = $O(log N)$ and Span = $O(log N)$


2a) Consider N = 6 with denominations {1, 3, 4}: The greedy algorithm would choose one coin valued at 4 first, skip 3, then two coins valued at 1, resulting in 3 coins, but a more optimal solution would be two coins valued at 3, which gives the same amount (6) with less coins.

2b) The optimal change to create for an amount N comes from the optimal solutions to problems less than N. If you know all minimum coin amounts required for all amounts less than N, then the optimal number of coins for N can be determined by adding one coin to the minimum of the optimal solutions for N−D_i for each denomination D_i that is available.

2c) A top down approach utilizing memoization stores the solutions of sub-problems to avoid redundant computations with a work of O(Nk) and a span of O(Nk).



