# LeetCode Two Sum Problem - Complete Solution in C

## 📋 Overview
This repository contains a **complete solution to the Two Sum problem from LeetCode**, implemented in **C programming language** with detailed documentation, explanations, and test cases. This is a beginner-friendly resource for learning problem-solving and coding interviews.

## 🎯 Problem Statement
Given an array of integers `nums` and an integer `target`, return the indices of the two numbers such that they add up to `target`.

- You may assume that each input would have **exactly one solution**
- You may not use the same element twice
- You can return the answer in any order

### Constraints
- `2 <= nums.length <= 10⁴`
- `-10⁹ <= nums[i] <= 10⁹`
- `-10⁹ <= target <= 10⁹`
- **Only one valid answer exists**

### Difficulty: **Easy** 🟢

## 💻 Why C Language?
**Author's Note:** This solution is implemented in **C language** because it is the primary language I'm currently learning and practicing. I'm proficient in C, while Python and Java are still being learned. This project serves as a practical application of my C programming knowledge for solving real LeetCode problems.

## 📁 Repository Structure
```
LeetCode-Two-Sum/
├── twoSum.c                    # C implementation of the solution
├── PROBLEM_DESCRIPTION.md      # Detailed problem statement and approaches
├── INPUT_OUTPUT_EXAMPLES.md    # Test cases with examples
├── SOLUTION_EXPLANATION.md     # Step-by-step code breakdown
├── COMPLEXITY_ANALYSIS.md      # Time and space complexity analysis
├── EDGE_CASES.md              # Edge cases and testing strategy
├── HASH_MAP_APPROACH.md       # Optimal O(n) hash map solution (reference)
├── IMPLEMENTATION_NOTES.md    # C language specific notes
├── COMMON_MISTAKES.md         # Common pitfalls and how to avoid them
├── LEETCODE_TIPS.md          # LeetCode problem-solving tips
├── INTERVIEW_PREP.md         # Interview preparation guide
├── PERFORMANCE_TIPS.md       # Performance optimization techniques
├── VARIATIONS.md             # Related problems and variations
├── RESOURCES.md              # Learning resources and references
├── FINAL_NOTES.md           # Summary and next steps
├── README.md                 # This file
└── JAVA_SOLUTION.java        # Reference implementation (Java)
└── PYTHON_SOLUTION.py        # Reference implementation (Python)
```

## 💡 Solution Code

### Approach: Brute Force (Two Nested Loops)
**File:** `twoSum.c`

The solution uses a straightforward **brute force approach**:
1. Iterate through each element in the array using an outer loop
2. For each element at index `i`, iterate through all elements after it using an inner loop starting from `i+1`
3. Check if the sum of the current pair equals the target
4. If a match is found, return the indices
5. If no pair found, return NULL

### Complexity Analysis
- **Time Complexity:** O(n²) - Two nested loops iterating through the array
- **Space Complexity:** O(1) - Only using a constant amount of extra space (excluding the output array)

### Performance Metrics
- **Status:** ✅ Accepted
- **Runtime:** 103 ms
- **Runtime Percentile:** Beats 32.38% of submissions
- **Memory Usage:** 8.58 MB
- **Memory Percentile:** Beats 93.07% of submissions
- **Test Cases Passed:** 63/63

## 📊 Examples

### Example 1
**Input:** `nums = [2,7,11,15], target = 9`
**Output:** `[0,1]`
**Explanation:** nums[0] + nums[1] == 9, we return [0, 1]

### Example 2
**Input:** `nums = [3,2,4], target = 6`
**Output:** `[1,2]`
**Explanation:** nums[1] + nums[2] == 6, we return [1, 2]

### Example 3
**Input:** `nums = [3,3], target = 6`
**Output:** `[0,1]`
**Explanation:** nums[0] + nums[1] == 6, we return [0, 1]

## 🚀 Alternative Approaches

### Hash Map Approach (Optimal - O(n))
**Time Complexity:** O(n)
**Space Complexity:** O(n)

Using a hash map/hash table to store value-to-index mappings:
1. Create a hash map to store values and their indices
2. For each number, check if (target - current_number) exists in the hash map
3. If found, return the indices
4. Otherwise, add the current number to the hash map

This approach reduces time complexity to O(n) with a single pass through the array.

## 📌 Key Concepts
- **Arrays and Indexing**
- **Nested Loops**
- **Hash Tables/Hash Maps**
- **Two Pointer Technique**
- **Time and Space Complexity Optimization**
- **C Memory Management (malloc)**
- **Dynamic Arrays in C**

## 🎓 Learning Topics
- Problem Analysis and Breakdown
- Algorithm Design Patterns
- Optimization Techniques
- Memory Management in C
- Dynamic Array Allocation
- Code Efficiency

## 📖 Documentation Files
- **[PROBLEM_DESCRIPTION.md](PROBLEM_DESCRIPTION.md)** - Detailed problem explanation and approaches
- **[INPUT_OUTPUT_EXAMPLES.md](INPUT_OUTPUT_EXAMPLES.md)** - Test cases and expected outputs
- **[SOLUTION_EXPLANATION.md](SOLUTION_EXPLANATION.md)** - Step-by-step code walkthrough
- **[twoSum.c](twoSum.c)** - Complete C source code with comments

## 🔗 Related LeetCode Problems
- Two Sum II - Input Array Is Sorted
- Two Sum III - Data Structure Design
- 3Sum
- 4Sum
- Two Sum IV - Input is a BST
- Two Sum Less Than K

## 💡 Tips for Problem Solving
1. Read the problem carefully and understand all constraints
2. Identify the problem pattern and think of multiple approaches
3. Start with a brute force solution first
4. Analyze time and space complexity
5. Optimize step by step
6. Test with edge cases
7. Practice regularly with different problems

## 📝 How to Use This Repository
1. Read the problem statement in `PROBLEM_DESCRIPTION.md`
2. Study the test cases in `INPUT_OUTPUT_EXAMPLES.md`
3. Review the C implementation in `twoSum.c`
4. Try implementing it yourself first
5. Compare your solution with the provided approach
6. Explore the optimization techniques
7. Practice solving similar problems

## 🎯 Learning Resources
For deeper learning:
- **LeetCode:** Official problem and discussions
- **GeeksforGeeks:** DSA tutorials
- **HackerRank:** Practice problems
- **YouTube:** Code with Harry, Striver's DSA course

## 📧 Author's Note
This repository is a learning project created while preparing for technical interviews and building strong problem-solving skills in C programming. Each file contains detailed explanations to help beginners understand not just the solution, but the thought process behind it.

---

**Happy Learning! 🚀**
*Keep practicing, keep improving!*
