# Remove Element

This is a solution for the "Remove Element" problem on LeetCode using Python.

## Problem Description

Given an array `nums` and a value `val`, you need to remove all instances of that value in-place and return the new length of the array. Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

The order of elements can be changed. It doesn't matter what you leave beyond the new length.

## Example

```python
Input: nums = [3, 2, 2, 3], val = 3
Output: 2
Explanation: Your function should return length = 2, with the first two elements of nums being 2.
```

## Approach

1. Initialize two pointers `i` and `j`, where `i` is the slow-runner and `j` is the fast-runner.
2. Iterate through the array.
3. If `nums[j]` is equal to the target value, increment `j` to skip over it.
4. If `nums[j]` is not equal to the target value, set `nums[i] = nums[j]`, then increment both `i` and `j`.
5. Continue this process until `j` reaches the end of the array.
6. The new length will be `i`.

## Usage

```python
nums = [3, 2, 2, 3]
val = 3
result = remove_element(nums, val)
print(result)  # Output: 2
```

## Complexity Analysis

The time complexity for this approach is O(n), where n is the length of the input array `nums`. The space complexity is O(1) as we are using a constant amount of extra memory.
