----------------------------------------------------------
# 136. Single Number
----------------------------------------------------------
## Problem Statement

Given a non-empty array of integers, every element appears twice except for one.
Find the element that appears only once.

Example:

Input:
nums = [4,1,2,1,2]

Output:
4


---

# Approach

## Initial Thinking

Need to find the number which appears only once.

Constraints:

- Time Complexity: O(n)
- Space Complexity: O(1)

So common approaches:

### 1. Sorting

Sort the array and compare adjacent elements.

Complexity:
- Time: O(n log n)
- Space: O(1)

Not suitable because time requirement is O(n).


### 2. Hash Map

Store frequency of each element.

Example:

4 -> 1
1 -> 2
2 -> 2

Complexity:
- Time: O(n)
- Space: O(n)

Not suitable because extra space is not allowed.


---

# Pattern Recognition

Need an operation where duplicate numbers cancel each other.

Bitwise XOR has this property:


------------

### 3  Algorithm

Initialize result = 0
Traverse every number
Combine result with current number using XOR
After traversal, result contains the single number

Example:

result = 0

0 ^ 4  = 4
4 ^ 1  = 5
5 ^ 2  = 7
7 ^ 1  = 6
6 ^ 2  = 4
==================================================================================================

# 268 Missing Number



