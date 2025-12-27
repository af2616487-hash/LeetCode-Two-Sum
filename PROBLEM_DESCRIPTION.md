# Two Sum - LeetCode Problem

## Problem Statement
Given an array of integers `nums` and an integer `target`, return the indices of the two numbers such that they add up to `target`.

You may assume that each input would have **exactly one solution**, and you may not use the same element twice.

You can return the answer in any order.

## Constraints
- 2 <= nums.length <= 10⁴
- -10⁹ <= nums[i] <= 10⁹
- -10⁹ <= target <= 10⁹
- **Only one valid answer exists.**

## Difficulty
**Easy**

## Topics
- Array
- Hash Table

## Approach Used
**Brute Force (Two Nested Loops)**

The solution uses a straightforward brute force approach:
1. Iterate through each element in the array using an outer loop
2. For each element at index `i`, iterate through all elements after it using an inner loop starting from `i+1`
3. Check if the sum of the current pair equals the target
4. If a match is found, return the indices
5. If no pair found, return NULL

## Complexity Analysis
- **Time Complexity:** O(n²) - Two nested loops iterating through the array
- **Space Complexity:** O(1) - Only using a constant amount of extra space (excluding the output array)

## Alternative Approaches

### Hash Map Approach (Optimal)
**Time Complexity:** O(n)
**Space Complexity:** O(n)

Using a hash map/hash table to store the difference and indices:
1. Create a hash map to store value-to-index mappings
2. For each number, check if (target - current_number) exists in the hash map
3. If found, return the indices
4. Otherwise, add the current number to the hash map

This reduces time complexity to O(n) with one pass through the array.
