# 67. Plus two

## Problem:
You are given a large integer represented as an integer array digits, where each digits[i] is the ith digit of the integer. The digits are ordered from most significant to least significant in left-to-right order. The large integer does not contain any leading 0's.

Increment the large integer by one and return the resulting array of digits.

 

Example 1:

Input: digits = [1,2,3]
Output: [1,2,4]
Explanation: The array represents the integer 123.
Incrementing by one gives 123 + 1 = 124.
Thus, the result should be [1,2,4].
Example 2:

Input: digits = [4,3,2,1]
Output: [4,3,2,2]
Explanation: The array represents the integer 4321.
Incrementing by one gives 4321 + 1 = 4322.
Thus, the result should be [4,3,2,2].
Example 3:

Input: digits = [9]
Output: [1,0]
Explanation: The array represents the integer 9.
Incrementing by one gives 9 + 1 = 10.
Thus, the result should be [1,0].

## Notes:
Intuition
The only trick here is in case one of the digits is 9. If so, we need to carry it to the next digit. If there are only 9's, we need to place a 1 at the beginning of the array.

Approach
We start by the end of the array using a for loop for (let i = digits.length - 1; i >= 0; i--)

If the current digit is less than 9, we increment digits[i] and return the array.

If digits[i] is 9, we set it to 0 and continue to the next digit (carry the 1).

If we finish the loop without returning, it means the entire number was made of 9s. In that case, we use unshift(1) to add the carry at the start.

Complexity
Time complexity:
O(n) — Worst case, we loop through all digits if they are all 9s.

Space complexity:
O(1) — We modify the input array in-place without using extra space, except for the final carry which adds one digit.