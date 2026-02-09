#  LeetCode 645: Set Mismatch

##  Problem Statement
You have a set of integers originally containing numbers from `1` to `n`. Due to an error, one number is duplicated, and one number goes missing. 

Find the **duplicate** and the **missing** number.

[View Problem on LeetCode](https://leetcode.com)

### Example
**Input:** `nums = [1,2,2,4]`  
**Output:** `[2,3]`  
**Explanation:** 2 is repeated, and 3 is missing from the sequence 1-4.

##  Intuition & Approach
Since the numbers are in a known range ($1$ to $n$), we can use a **frequency array** (or hash bucket) to count how many times each number appears.

1. **Count Frequencies:** Create a `count` array of size `n + 1`.
2. **Scan Input:** Iterate through `nums` and increment the index in `count` corresponding to each number.
3. **Identify Error:** 
   - The index with a value of `2` is our **duplicate**.
   - The index with a value of `0` is our **missing** number.

Complexity Analysis
Time Complexity: \(O(n)\) — We traverse the input array once and the frequency array once.
Space Complexity: \(O(n)\) — We allocate an extra array of size \(n+1\) to store counts. 
