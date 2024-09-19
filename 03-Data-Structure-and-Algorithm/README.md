# 3. **Data Structures and Algorithms (DSA)**

#### 1. **Arrays and Strings**
   - **Manipulation:**
     - Access: O(1)
     - Search: O(n)
     - Insertion/Deletion: O(n) (for shifting elements)
   - **Subarrays:**
     - Finding all subarrays: O(n^2)
   - **Anagrams:**
     - Checking if two strings are anagrams: O(n)
   - **Palindromes:**
     - Checking if a string is a palindrome: O(n)

   **Real-World Example:** Arrays are used in image processing where pixel values are stored in arrays, and operations such as rotation or flipping involve manipulation of array elements.

---

#### 2. **Linked Lists**
   - **Singly Linked List:**
     - Access: O(n)
     - Search: O(n)
     - Insertion/Deletion: O(1) (at head)
   - **Doubly Linked List:**
     - Access: O(n)
     - Search: O(n)
     - Insertion/Deletion: O(1) (at head/tail)
   - **Circular Linked List:**
     - Access: O(n)
     - Search: O(n)
   - **Reversing:**
     - O(n)
   - **Detecting Loops:**
     - Floyd’s Cycle Detection: O(n)

   **Real-World Example:** Linked lists are used in the implementation of a music player’s playlist where the playlist can be traversed forward and backward.

---

#### 3. **Stacks and Queues**
   - **Implementation:**
     - Push/Pop (Stack): O(1)
     - Enqueue/Dequeue (Queue): O(1)
   - **Infix/Postfix Expressions:**
     - Evaluation: O(n)
   - **LRU Cache:**
     - Insertion/Access: O(1) (using hash map and doubly linked list)

   **Real-World Example:** Stacks are used in undo operations in text editors, and queues are used in task scheduling systems.

---

#### 4. **Hashing**
   - **Hash Tables/Hash Maps:**
     - Access/Search/Insert: O(1) (average case)
   - **Collision Handling:**
     - Chaining: O(n) (in worst case)
     - Open Addressing: O(n) (in worst case)

   **Real-World Example:** Hash maps are used in databases to quickly locate data entries.

---

#### 5. **Trees**
   - **Binary Trees:**
     - Traversal: O(n)
   - **Binary Search Trees (BST):**
     - Search/Insert/Delete: O(log n) (average case)
   - **AVL Trees:**
     - Search/Insert/Delete: O(log n)
   - **Segment Trees:**
     - Query/Update: O(log n)
   - **Tries:**
     - Insert/Search: O(m) (where m is the length of the key)

   **Real-World Example:** AVL trees are used in balanced search trees for efficient data retrieval, and tries are used for autocomplete systems.

---

#### 6. **Graphs**
   - **BFS/DFS:**
     - Time Complexity: O(V + E) (where V is vertices and E is edges)
   - **Dijkstra’s Algorithm:**
     - Time Complexity: O(V^2) (with adjacency matrix), O((V + E) log V) (with priority queue)
   - **Topological Sorting:**
     - Time Complexity: O(V + E)
   - **Cycle Detection:**
     - DFS-based: O(V + E)

   **Real-World Example:** BFS is used in social network analysis to find the shortest path between friends.

---

#### 7. **Heaps**
   - **Min Heap/Max Heap:**
     - Insert/Delete: O(log n)
     - Find Min/Max: O(1)
   - **Heap Sort:**
     - Time Complexity: O(n log n)

   **Real-World Example:** Heaps are used in priority queues, such as in scheduling tasks with varying priorities.

---

#### 8. **Sorting Algorithms**
   - **Merge Sort:**
     - Time Complexity: O(n log n)
   - **Quicksort:**
     - Time Complexity: O(n log n) (average case), O(n^2) (worst case)
   - **Bubble Sort:**
     - Time Complexity: O(n^2)
   - **Insertion Sort:**
     - Time Complexity: O(n^2)
   - **Radix Sort:**
     - Time Complexity: O(nk) (where k is the number of digits in the largest number)

   **Real-World Example:** Merge sort is used in external sorting where large files are sorted using merge operations.

---

#### 9. **Searching Algorithms**
   - **Binary Search:**
     - Time Complexity: O(log n) (for sorted arrays)
   - **Linear Search:**
     - Time Complexity: O(n)
   - **Ternary Search:**
     - Time Complexity: O(log n)

   **Real-World Example:** Binary search is used in library databases to quickly locate a book by its index.

---

#### 10. **Dynamic Programming**
   - **Memoization/Tabulation:**
     - Time Complexity: O(n) for many problems
   - **Common Problems:**
     - Knapsack Problem: O(nW) (where W is the maximum weight)
     - Longest Common Subsequence (LCS): O(n*m) (where n and m are lengths of the sequences)
     - Longest Increasing Subsequence (LIS): O(n^2) (with DP), O(n log n) (with patience sorting)

   **Real-World Example:** Dynamic programming is used in financial planning and resource allocation problems.

---

#### 11. **Greedy Algorithms**
   - **Huffman Coding:**
     - Time Complexity: O(n log n)
   - **Activity Selection:**
     - Time Complexity: O(n log n) (sorting), O(n) (selection)
   - **Fractional Knapsack:**
     - Time Complexity: O(n log n) (sorting)

   **Real-World Example:** Greedy algorithms are used in optimization problems like minimizing the cost of resource allocation.

---

#### 12. **Backtracking**
   - **N-Queens:**
     - Time Complexity: O(n!)
   - **Sudoku Solver:**
     - Time Complexity: O(9^m) (where m is the number of cells to fill)
   - **Subset Sum:**
     - Time Complexity: O(2^n)

   **Real-World Example:** Backtracking is used in puzzle solving and constraint satisfaction problems.

---

#### 13. **Bit Manipulation**
   - **Bitwise Operators:**
     - Time Complexity: O(1)
   - **Bit Masking:**
     - Time Complexity: O(1)
   - **Counting Bits:**
     - Time Complexity: O(log n)

   **Real-World Example:** Bit manipulation is used in low-level programming, cryptography, and efficient algorithms for counting set bits.

---
