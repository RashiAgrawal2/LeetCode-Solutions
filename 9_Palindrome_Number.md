# 9. Palindrome Number

**LeetCode Link**: https://leetcode.com/problems/palindrome-number/

## Problem Description
Given an integer x, return true if x is a palindrome, and false otherwise.

## Solution
```cpp
class Solution {
public:
    bool isPalindrome(int x) {
        if (x < 0) return false;
        
        long reversed = 0;
        long num = x;
        
        while (num > 0) {
            reversed = reversed * 10 + num % 10;
            num /= 10;
        }
        
        return reversed == x;
    }
};
```

## Complexity Analysis
- **Time Complexity**: O(log n) where n is the number
- **Space Complexity**: O(1)
