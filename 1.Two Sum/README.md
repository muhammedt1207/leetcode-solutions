# 1. Two Sum

## Problem:
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

 

Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]
Example 3:

Input: nums = [3,3], target = 6
Output: [0,1]

## Notes:
This is the first easy question in LeetCode. Yes, it's very EASY.

Before we jump to coding let's learn how to analyse the description, because this will help us to find the gaps and figure out the hints which are the half of the solution.

In the descrition they give us the type of our input which is an array and we require us to return the indices (indexes).

As we know if we want to return indexes or elements of an array we can use for loop (There other ways), and to return the indices in the format of [indice1,indice2] we need to put them in an array. GOOD!

In the description there is hint which is :

You may assume that each input would have exactly one solution

One solution means you can find only two destinct indices. NOTHING ELSE.

Also, there is other hint:

You can return the answer in any order.

It means we car return : [i1,i1] or [i2,i1]. They made it easy for us.

We will use two nested loops as given in the illustration bellow: