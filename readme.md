# 📝 Interview Preparation Checklist

## 📚 Table of Contents
1. [Arrays](#1-arrays)
2. [Strings](#2-strings)
3. [Linked Lists](#3-linked-lists)
4. [Stacks and Queues](#4-stacks-and-queues)
5. [Trees](#5-trees)
6. [Graphs](#6-graphs)
7. [Dynamic Programming](#7-dynamic-programming)
8. [Backtracking](#8-backtracking)
9. [Sorting and Searching](#9-sorting-and-searching)
10. [Bit Manipulation](#10-bit-manipulation)

---

<details>
<summary><strong>1. Arrays</strong></summary>

### Easy Problems
- [ ] [Two Sum](https://leetcode.com/problems/two-sum/)
- [ ] [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- [ ] [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
- [ ] [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- [ ] [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- [ ] [Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- [ ] [Rotate Array](https://leetcode.com/problems/rotate-array/)
- [ ] [Plus One](https://leetcode.com/problems/plus-one/)
- [ ] [Intersection of Two Arrays II](https://leetcode.com/problems/intersection-of-two-arrays-ii/)
- [ ] [Find All Numbers Disappeared in an Array](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/)
- [ ] [Single Number](https://leetcode.com/problems/single-number/)
- [ ] [Majority Element](https://leetcode.com/problems/majority-element/)
- [ ] [Pascal's Triangle](https://leetcode.com/problems/pascals-triangle/)
- [ ] [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/)
- [ ] [Rotate Image](https://leetcode.com/problems/rotate-image/)

### Medium Problems
- [ ] [3Sum](https://leetcode.com/problems/3sum/)
- [ ] [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/)
- [ ] [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- [ ] [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- [ ] [Word Search](https://leetcode.com/problems/word-search/)

### Hard Problems
- [ ] [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- [ ] [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
- [ ] [First Missing Positive](https://leetcode.com/problems/first-missing-positive/)
- [ ] [Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- [ ] [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)

### Notes
- **Two Pointer Technique**: Useful for problems involving sorted arrays or finding pairs.
- **Sliding Window**: Great for problems involving subarrays or substrings.
- **Hash Maps**: Efficient for counting occurrences or finding duplicates.

```typescript
function twoSum(nums: number[], target: number): number[] {
    let left = 0, right = nums.length - 1;
    while (left < right) {
        const sum = nums[left] + nums[right];
        if (sum === target) return [left, right];
        else if (sum < target) left++;
        else right--;
    }
    return [];
}
