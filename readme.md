// README.md

// # Interview Preparation Checklist

// ## Table of Contents
// 1. [Arrays](#arrays)
// 2. [Strings](#strings)
// 3. [Linked Lists](#linked-lists)
// 4. [Stacks and Queues](#stacks-and-queues)
// 5. [Trees](#trees)
// 6. [Graphs](#graphs)
// 7. [Dynamic Programming](#dynamic-programming)
// 8. [Backtracking](#backtracking)
// 9. [Sorting and Searching](#sorting-and-searching)
// 10. [Bit Manipulation](#bit-manipulation)

// ---

// <details>
// <summary><strong>1. Arrays</strong></summary>

// ### Easy Problems
// - [ ] [Two Sum](https://leetcode.com/problems/two-sum/)
// - [ ] [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
// - [ ] [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
// - [ ] [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
// - [ ] [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
// - [ ] [Move Zeroes](https://leetcode.com/problems/move-zeroes/)
// - [ ] [Rotate Array](https://leetcode.com/problems/rotate-array/)
// - [ ] [Plus One](https://leetcode.com/problems/plus-one/)
// - [ ] [Intersection of Two Arrays II](https://leetcode.com/problems/intersection-of-two-arrays-ii/)
// - [ ] [Find All Numbers Disappeared in an Array](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/)
// - [ ] [Single Number](https://leetcode.com/problems/single-number/)
// - [ ] [Majority Element](https://leetcode.com/problems/majority-element/)
// - [ ] [Pascal's Triangle](https://leetcode.com/problems/pascals-triangle/)
// - [ ] [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/)
// - [ ] [Rotate Image](https://leetcode.com/problems/rotate-image/)

// ### Medium Problems
// - [ ] [3Sum](https://leetcode.com/problems/3sum/)
// - [ ] [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/)
// - [ ] [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
// - [ ] [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
// - [ ] [Word Search](https://leetcode.com/problems/word-search/)

// ### Hard Problems
// - [ ] [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
// - [ ] [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
// - [ ] [First Missing Positive](https://leetcode.com/problems/first-missing-positive/)
// - [ ] [Merge Intervals](https://leetcode.com/problems/merge-intervals/)
// - [ ] [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)

// ### Notes
// - **Two Pointer Technique**: Useful for problems involving sorted arrays or finding pairs.
// - **Sliding Window**: Great for problems involving subarrays or substrings.
// - **Hash Maps**: Efficient for counting occurrences or finding duplicates.

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

// </details>

// <details>
// <summary><strong>2. Strings</strong></summary>

// ### Easy Problems
// - [ ] [Reverse String](https://leetcode.com/problems/reverse-string/)
// - [ ] [Valid Anagram](https://leetcode.com/problems/valid-anagram/)
// - [ ] [First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
// - [ ] [Implement strStr()](https://leetcode.com/problems/implement-strstr/)
// - [ ] [Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
// - [ ] [Palindrome Permutation](https://leetcode.com/problems/palindrome-permutation/)
// - [ ] [String Compression](https://leetcode.com/problems/string-compression/)
// - [ ] [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
// - [ ] [Ransom Note](https://leetcode.com/problems/ransom-note/)
// - [ ] [Repeated Substring Pattern](https://leetcode.com/problems/repeated-substring-pattern/)
// - [ ] [Add Strings](https://leetcode.com/problems/add-strings/)
// - [ ] [Reverse Words in a String III](https://leetcode.com/problems/reverse-words-in-a-string-iii/)
// - [ ] [Detect Capital](https://leetcode.com/problems/detect-capital/)
// - [ ] [Longest Palindrome](https://leetcode.com/problems/longest-palindrome/)
// - [ ] [Count and Say](https://leetcode.com/problems/count-and-say/)

// ### Medium Problems
// - [ ] [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
// - [ ] [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
// - [ ] [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
// - [ ] [Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
// - [ ] [Generate Parentheses](https://leetcode.com/problems/generate-parentheses/)

// ### Hard Problems
// - [ ] [Wildcard Matching](https://leetcode.com/problems/wildcard-matching/)
// - [ ] [Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/)
// - [ ] [Palindrome Pairs](https://leetcode.com/problems/palindrome-pairs/)
// - [ ] [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
// - [ ] [Substring with Concatenation of All Words](https://leetcode.com/problems/substring-with-concatenation-of-all-words/)

// ### Notes
// - **Two Pointer Technique**: Useful for problems involving palindromes or reversing strings.
// - **Hash Maps**: Efficient for counting character frequencies or checking anagrams.
// - **Sliding Window**: Great for substring problems.

function lengthOfLongestSubstring(s: string): number {
    const map = new Map<string, number>();
    let left = 0, maxLength = 0;
    
    for (let right = 0; right < s.length; right++) {
        if (map.has(s[right])) {
            left = Math.max(map.get(s[right])! + 1, left);
        }
        map.set(s[right], right);
        maxLength = Math.max(maxLength, right - left + 1);
    }
    
    return maxLength;
}

// </details>

// <details>
// <summary><strong>3. Linked Lists</strong></summary>

// ### Easy Problems
// - [ ] [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
// - [ ] [Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list/)
// - [ ] [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
// - [ ] [Remove Duplicates from Sorted List](https://leetcode.com/problems/remove-duplicates-from-sorted-list/)
// - [ ] [Delete Node in a Linked List](https://leetcode.com/problems/delete-node-in-a-linked-list/)
// - [ ] [Palindrome Linked List](https://leetcode.com/problems/palindrome-linked-list/)
// - [ ] [Intersection of Two Linked Lists](https://leetcode.com/problems/intersection-of-two-linked-lists/)
// - [ ] [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
// - [ ] [Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)
// - [ ] [Remove Linked List Elements](https://leetcode.com/problems/remove-linked-list-elements/)
// - [ ] [Convert Binary Number in a Linked List to Integer](https://leetcode.com/problems/convert-binary-number-in-a-linked-list-to-integer/)
// - [ ] [Design Linked List](https://leetcode.com/problems/design-linked-list/)
// - [ ] [Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
// - [ ] [Add Two Numbers](https://leetcode.com/problems/add-two-numbers/)
// - [ ] [Swap Nodes in Pairs](https://leetcode.com/problems/swap-nodes-in-pairs/)

// ### Medium Problems
// - [ ] [Odd Even Linked List](https://leetcode.com/problems/odd-even-linked-list/)
// - [ ] [Linked List Components](https://leetcode.com/problems/linked-list-components/)
// - [ ] [Reorder List](https://leetcode.com/problems/reorder-list/)
// - [ ] [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)
// - [ ] [Rotate List](https://leetcode.com/problems/rotate-list/)

// ### Hard Problems
// - [ ] [Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
// - [ ] [Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/)
// - [ ] [Copy List with Random Pointer](https://leetcode.com/problems/copy-list-with-random-pointer/)
// - [ ] [LRU Cache](https://leetcode.com/problems/lru-cache/)
// - [ ] [Sort List](https://leetcode.com/problems/sort-list/)

// ### Notes
// - **Fast and Slow Pointers**: Useful for detecting cycles and finding the middle of the list.
// - **Dummy Nodes**: Simplify edge cases in insertion and deletion.
// - **Reversal Techniques**: Important for reversing linked lists or sublists.

function hasCycle(head: ListNode | null): boolean {
    if (!head || !head.next) return false;
    let slow = head, fast = head.next;
    while (slow !== fast) {
        if (!fast || !fast.next) return false;
        slow = slow.next!;
        fast = fast.next.next!;
    }
    return true;
}

// </details>

// <details>
// <summary><strong>4. Stacks and Queues</strong></summary>

// ### Easy Problems
// - [ ] [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
// - [ ] [Min Stack](https://leetcode.com/problems/min-stack/)
// - [ ] [Implement Queue using Stacks](https://leetcode.com/problems/implement-queue-using-stacks/)
// - [ ] [Implement Stack using Queues](https://leetcode.com/problems/implement-stack-using-queues/)
// - [ ] [Baseball Game](https://leetcode.com/problems/baseball-game/)
// - [ ] [Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/)
// - [ ] [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)
// - [ ] [Remove All Adjacent Duplicates In String](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string/)
// - [ ] [Backspace String Compare](https://leetcode.com/problems/backspace-string-compare/)
// - [ ] [Circular Queue](https://leetcode.com/problems/design-circular-queue/)
// - [ ] [Moving Average from Data Stream](https://leetcode.com/problems/moving-average-from-data-stream/)
// - [ ] [Next Greater Element II](https://leetcode.com/problems/next-greater-element-ii/)
// - [ ] [Design Circular Deque](https://leetcode.com/problems/design-circular-deque/)
// - [ ] [Decode String](https://leetcode.com/problems/decode-string/)
// - [ ] [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/)

// ### Medium Problems
// - [ ] [Binary Tree Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/)
// - [ ] [Binary Tree Preorder Traversal](https://leetcode.com/problems/binary-tree-preorder-traversal/)
// - [ ] [Binary Tree Postorder Traversal](https://leetcode.com/problems/binary-tree-postorder-traversal/)
// - [ ] [Design Browser History](https://leetcode.com/problems/design-browser-history/)
// - [ ] [LRU Cache](https://leetcode.com/problems/lru-cache/)

// ### Hard Problems
// - [ ] [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)
// - [ ] [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
// - [ ] [Basic Calculator](https://leetcode.com/problems/basic-calculator/)
// - [ ] [Basic Calculator II](https://leetcode.com/problems/basic-calculator-ii/)
// - [ ] [Expression Add Operators](https://leetcode.com/problems/expression-add-operators/)

// ### Notes
// - **Stack Usage**: Useful for problems involving LIFO order, such as parsing expressions or managing function calls.
// - **Queue Usage**: Useful for problems involving FIFO order, such as breadth-first search or task scheduling.
// - **Monotonic Stack**: Useful for finding the next greater or smaller element.

function nextGreaterElements(nums: number[]): number[] {
    const stack: number[] = [];
    const result = new Array(nums.length).fill(-1);
    
    for (let i = 0; i < nums.length * 2; i++) {
        const num = nums[i % nums.length];
        while (stack.length && nums[stack[stack.length - 1]] < num) {
            result[stack.pop()!] = num;
        }
        if (i < nums.length) stack.push(i);
    }
    
    return result;
}

// </details>

// <details>
// <summary><strong>5. Trees</strong></summary>

// ### Easy Problems
// - [ ] [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)
// - [ ] [Symmetric Tree](https://leetcode.com/problems/symmetric-tree/)
// - [ ] [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
// - [ ] [Convert Sorted Array to Binary Search Tree](https://leetcode.com/problems/convert-sorted-array-to-binary-search-tree/)
// - [ ] [Path Sum](https://leetcode.com/problems/path-sum/)
// - [ ] [Same Tree](https://leetcode.com/problems/same-tree/)
// - [ ] [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
// - [ ] [Balanced Binary Tree](https://leetcode.com/problems/balanced-binary-tree/)
// - [ ] [Minimum Depth of Binary Tree](https://leetcode.com/problems/minimum-depth-of-binary-tree/)
// - [ ] [Binary Tree Paths](https://leetcode.com/problems/binary-tree-paths/)
// - [ ] [Sum of Left Leaves](https://leetcode.com/problems/sum-of-left-leaves/)
// - [ ] [Binary Tree Tilt](https://leetcode.com/problems/binary-tree-tilt/)
// - [ ] [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
// - [ ] [Subtree of Another Tree](https://leetcode.com/problems/subtree-of-another-tree/)
// - [ ] [Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)

// ### Medium Problems
// - [ ] [Binary Tree Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/)
// - [ ] [Binary Tree Preorder Traversal](https://leetcode.com/problems/binary-tree-preorder-traversal/)
// - [ ] [Binary Tree Postorder Traversal](https://leetcode.com/problems/binary-tree-postorder-traversal/)
// - [ ] [Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)
// - [ ] [Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/)

// ### Hard Problems
// - [ ] [Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
// - [ ] [Recover Binary Search Tree](https://leetcode.com/problems/recover-binary-search-tree/)
// - [ ] [Binary Tree Cameras](https://leetcode.com/problems/binary-tree-cameras/)
// - [ ] [Count Complete Tree Nodes](https://leetcode.com/problems/count-complete-tree-nodes/)
// - [ ] [Redundant Connection II](https://leetcode.com/problems/redundant-connection-ii/)

// ### Notes
// - **Tree Traversals**: Inorder, Preorder, and Postorder traversals are fundamental.
// - **Recursion**: Commonly used for tree problems due to the recursive nature of trees.
// - **Binary Search Tree (BST) Properties**: Useful for problems involving searching and sorting.

function inorderTraversal(root: TreeNode | null): number[] {
    const result: number[] = [];
    function traverse(node: TreeNode | null) {
        if (!node) return;
        traverse(node.left);
        result.push(node.val);
        traverse(node.right);
    }
    traverse(root);
    return result;
}

// </details>

// <details>
// <summary><strong>6. Graphs</strong></summary>

// ### Easy Problems
// - [ ] [Find the Town Judge](https://leetcode.com/problems/find-the-town-judge/)
// - [ ] [Flood Fill](https://leetcode.com/problems/flood-fill/)
// - [ ] [Number of Islands](https://leetcode.com/problems/number-of-islands/)
// - [ ] [Max Area of Island](https://leetcode.com/problems/max-area-of-island/)
// - [ ] [Clone Graph](https://leetcode.com/problems/clone-graph/)
// - [ ] [Course Schedule](https://leetcode.com/problems/course-schedule/)
// - [ ] [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
// - [ ] [Graph Valid Tree](https://leetcode.com/problems/graph-valid-tree/)
// - [ ] [Network Delay Time](https)
