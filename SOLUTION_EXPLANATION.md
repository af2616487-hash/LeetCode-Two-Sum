# Solution Explanation - Two Sum Problem

## Step-by-Step Breakdown

### Function Signature
```c
int* twoSum(int* nums, int numsSize, int target, int* returnSize)
```

### Parameters
- `nums`: Array of integers
- `numsSize`: Size of the array
- `target`: Target sum we're looking for
- `returnSize`: Pointer to return the size (always 2)

### Algorithm Steps

1. **Initialize returnSize**: Set it to 2 since we always return 2 indices
2. **Allocate memory**: Create an array of size 2 using malloc
3. **Nested loops**: 
   - Outer loop: iterate from i=0 to numsSize-1
   - Inner loop: iterate from j=i+1 to numsSize-1
4. **Check condition**: If nums[i] + nums[j] == target
5. **Return result**: Store indices in ans and return
6. **Edge case**: Return NULL if no pair found

## Code Walkthrough

```c
// Set return size
*returnSize = 2;

// Allocate memory for result
int* ans = (int*)malloc(2 * sizeof(int));

// Brute force: check all pairs
for (int i = 0; i < numsSize; i++) {      // First number
    for (int j = i + 1; j < numsSize; j++) { // Second number
        if (nums[i] + nums[j] == target) {
            ans[0] = i;   // First index
            ans[1] = j;   // Second index
            return ans;   // Found the pair
        }
    }
}
return NULL; // No pair found
```

## Example Trace

### Input: nums = [2,7,11,15], target = 9

| i | j | nums[i] | nums[j] | Sum | Equal to target? | Action |
|---|---|---------|---------|-----|------------------|--------|
| 0 | 1 | 2       | 7       | 9   | ✓ YES            | Return [0,1] |

### Why it works
- nums[0]=2, nums[1]=7
- 2 + 7 = 9 (matches target)
- Return indices [0, 1]

## Time Complexity: O(n²)
- Outer loop: n iterations
- Inner loop: up to n iterations
- Total: n × n = n²

## Space Complexity: O(1)
- Only allocating fixed size array (2 elements)
- No additional data structures

## Key Insights
1. Must check all pairs to guarantee finding the solution
2. j starts from i+1 to avoid using same element twice
3. Early return when pair is found improves average case
4. Works for all valid inputs due to constraint guarantee
