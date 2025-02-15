# Daily-Leetcode-problem-solution6

PROBLEM

Given a positive integer n, return the punishment number of n.
The punishment number of n is defined as the sum of the squares of all integers i such that:
1 <= i <= n
The decimal representation of i * i can be partitioned into contiguous substrings such that the sum of the integer values of these substrings equals i.

Intuition

Iterate through all numbers i from 1 to n:
Compute i * i (the square of i).
Convert i * i to a string to explore its partitions.
Check if i * i can be partitioned into contiguous substrings whose sum equals i:
Use a recursive function to explore all possible ways to split the string representation of i * i.
If a valid partitioning exists, add i * i to the result.
Return the sum of all valid squared numbers.

Approach

Iterate over numbers i from 1 to n, compute i², and check if it can be split into substrings summing to i.
canPartition function:
Recursively checks all partitions of i².
If a valid partitioning is found, return true.
If i² satisfies the condition, add it to the total sum.

Complexity

Time complexity:
O(nlogn)

Space complexity:
The space complexity of this solution is O(d), where d is the number of digits in i², due to recursion depth in canPartition.
 
