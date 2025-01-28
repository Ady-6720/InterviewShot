# 🚀 Java DSA Intensive Study Plan (2 Weeks)

A structured 2-week plan to master Data Structures and Algorithms (DSA) using Java, with daily practice on LeetCode. Designed for efficiency and clarity, with code examples and curated problem sets.

---

## 📅 **Weekly Schedule**

### **Week 1: Core Data Structures**

| Day | Topic                | Key Concepts                                                                 | Practice Problems                                                                                                                                 |
|-----|----------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | **Arrays & Strings** | Sliding window, two-pointer technique, `StringBuilder`                      | [Reverse String](https://leetcode.com/problems/reverse-string/), [Container With Most Water](https://leetcode.com/problems/container-with-most-water/) |
| 2   | **Linked Lists**     | Dummy nodes, fast/slow pointers                                             | [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/), [Detect Cycle](https://leetcode.com/problems/linked-list-cycle/)           |
| 3   | **Stacks & Queues**  | Monotonic stacks, `Deque`                                                   | [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/), [Min Stack](https://leetcode.com/problems/min-stack/)                           |
| 4   | **Hash Tables**      | `HashMap`, frequency counting                                               | [Two Sum](https://leetcode.com/problems/two-sum/), [Group Anagrams](https://leetcode.com/problems/group-anagrams/)                                     |
| 5-6 | **Trees & BSTs**     | BFS/DFS traversal, BST validation                                           | [Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/), [Validate BST](https://leetcode.com/problems/validate-binary-search-tree/) |

---

### **Week 2: Algorithms & Advanced Topics**

| Day | Topic                  | Key Concepts                                                                 | Practice Problems                                                                                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| 7   | **Sorting & Searching**| MergeSort, Binary Search                                                    | [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/), [Find First/Last Position](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) |
| 8   | **Recursion & Backtracking** | Permutations, subsets                                                  | [Permutations](https://leetcode.com/problems/permutations/), [Subsets](https://leetcode.com/problems/subsets/)                                       |
| 9   | **Dynamic Programming**| Memoization, tabulation                                                     | [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/), [Coin Change](https://leetcode.com/problems/coin-change/)                           |
| 10  | **Graphs**             | BFS/DFS, adjacency lists                                                    | [Number of Islands](https://leetcode.com/problems/number-of-islands/), [Clone Graph](https://leetcode.com/problems/clone-graph/)                       |
| 11  | **Greedy & Bit Manipulation** | XOR tricks, greedy intuition                                          | [Single Number](https://leetcode.com/problems/single-number/), [Jump Game](https://leetcode.com/problems/jump-game/)                                   |
| 12-13 | **Mock Interviews**   | Timed practice (45 mins/problem)                                            | [LRU Cache](https://leetcode.com/problems/lru-cache/), [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/) |
| 14  | **Review & Refine**    | Focus on weaknesses                                                         | Revisit challenging problems from previous days.                                                                                                   |

---

## 🛠️ **Java-Specific Tips**
- Use `StringBuilder` instead of `String` for concatenation in loops.
- Avoid autoboxing (e.g., `Integer` ↔ `int`) in performance-critical code.
- Prefer `ArrayList` over raw arrays for dynamic resizing.
- Learn custom sorting with `Comparator`:
  ```java
  Arrays.sort(intervals, (a, b) -> a[0] - b[0]); // Sort 2D array by start time
