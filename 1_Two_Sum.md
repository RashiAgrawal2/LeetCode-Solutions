# 1. Two Sum

**LeetCode Link**: https://leetcode.com/problems/two-sum/

## Problem Description
Given an array of integers nums and an integer target, return the indices of the two numbers that add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.

## Solution
```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> seen;
        for (int i = 0; i < nums.size(); i++) {
            int complement = target - nums[i];
            if (seen.find(complement) != seen.end()) {
                return {seen[complement], i};
            }
            seen[nums[i]] = i;
        }
        return {};
    }
};
```

## Complexity Analysis
- **Time Complexity**: O(n) - Single pass through the array
- **Space Complexity**: O(n) - Hash map storage
