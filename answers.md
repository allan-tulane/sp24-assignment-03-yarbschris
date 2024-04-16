# CMPS 2200 Assignment 3
## Answers

**Name:** Christopher Yarbro


Place all written answers from `assignment-03.md` here for easier grading.

1a) Divide N by the largest currency demonimation 2^k to the largest whole number. The number of times 2^k divides into N is the number of 2^k coins. Then, take the remainder as the new N and divide by 2^k-1. If any N < 2^k then move on to 2^k-1. Recurse until N = 0. Sum of all counts of 2^k coins is the total number of coins

