# DSA
Algorithm and Data Structure

### Big O

| Big-O          | Name        | Example              |
| -------------- | ----------- | -------------------- |
| **O(1)**       | Constant    | Access array element |
| **O(log n)**   | Logarithmic | Binary Search        |
| **O(n)**       | Linear      | Single loop          |
| **O(n log n)** | Linear-Log  | Merge Sort           |
| **O(n²)**      | Quadratic   | Nested loops         |
| **O(2ⁿ)**      | Exponential | Recursive Fibonacci  |
| **O(n!)**      | Factorial   | Traveling Salesman   |

- O(1) = O(n^1) = constant (run in constant time)
- O(n) = linear (run in constant time)
- Complexity measures how efficiently an algorithm works.

### Abstract data type ( Array, Stack, Queue, Linked List)
- Elements in an array are accessed randomly. In Linked lists, elements are accessed sequentially.
- Underflow occurs when the user performs a pop operation on an empty stack.
- Overflow occurs when the stack is full and the user performs a push operation.
-  Garbage Collection is used to recover the memory occupied by objects that are no longer used.
  
```
What is the value of the postfix expression 6 3 2 4 + – *?
a) 1
b) 40
c) 74
d) -18
View Answer
Answer: d
Explanation: Postfix Expression is (6*(3-(2+4))) which results -18 as output.
```
```
Here is an infix expression: 4 + 3*(6*3-12). Suppose that we are using the usual stack algorithm to convert the expression from infix to postfix notation. The maximum number of symbols that will appear on the stack AT ONE TIME during the conversion of this expression?
a) 1
b) 2
c) 3
d) 4
View Answer
Answer: d
Explanation: When we perform the conversion from infix to postfix expression +, *, (, * symbols are placed inside the stack. A maximum of 4 symbols are identified during the entire conversion.
```

### Infix, Prefix & Postfix
- Notations to write an expression.
- 1. Infix = eg. a+b , a-b, p/v
  2. Prefix - eg. +ab, -ab, /pv
  3. Postfix - ab+, ab-, pv/

```
Eg. infix = A*(B+C)*D <br>
 Postfix - ABC +* D
first to solve parenthesis and then solve multiply in left side then right side.
EG. x-y*z to prefix and postfix?
1.prefix = -x*yz
2.postfix - xyz*-
```
- stack operation 2

## TREE
### 🌳 1. Introduction to Trees & Terminology
- A tree is a non-linear hierarchical data structure consisting of nodes connected by edges. <br>
One root node <br>
Remaining nodes form subtrees <br>

No cycles (acyclic)
<img width="1002" height="501" alt="image" src="https://github.com/user-attachments/assets/bf7620d9-3f3b-4563-b375-d88da0d544a8" />


| Term                 | Meaning                                   |
| -------------------- | ----------------------------------------- |
| Root                 | Topmost node                              |
| Parent               | Node having children                      |
| Child                | Node derived from parent                  |
| Siblings             | Nodes with same parent                    |
| Leaf (External node) | Node with no children                     |
| Internal node        | Node with at least one child              |
| Edge                 | Connection between nodes                  |
| Degree of node       | Number of children                        |
| Degree of tree       | Max degree of any node                    |
| Level                | Distance from root (root at level 0 or 1) |
| Height               | Longest path from node to leaf            |
| Depth                | Distance from root to node                |

```
MCQ Tip:
Tree with n nodes → n−1 edges
Height ≠ Depth (very common confusion)
```
### 🔁 2. Tree Traversals
- Traversal = Visiting each node exactly once.
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/ceecf3db-f26c-4a86-baa9-fe6fdc0a6826" />
```
Depth-First Traversals (DFS)
Preorder (Root → Left → Right)
Inorder (Left → Root → Right)
🔑 Gives sorted order in BST
Postorder (Left → Right → Root)

Breadth-First Traversal (BFS)
Level Order (Level by level)
```
| Traversal   | Used for            |
| ----------- | ------------------- |
| Preorder    | Copying tree        |
| Inorder     | Sorted output (BST) |
| Postorder   | Deleting tree       |
| Level Order | Heap, ACBT          |

- Inorder traversal of BST(Binary Search Tree) is always sorted. es — it means that when you perform an inorder traversal on a Binary Search Tree (BST), the output is always in sorted order.

```
A Binary Search Tree (BST) follows this rule:
- All values in the left subtree are smaller than the root
- All values in the right subtree are greater than the root



### 🌲 3. Binary Trees

```
A tree where each node has at most two children:
Left child
Right child

MCQ Trap:
Binary tree ≠ Binary Search Tree

```

| Type                | Property                      |
| ------------------- | ----------------------------- |
| Full Binary Tree    | Each node has 0 or 2 children |
| Perfect Binary Tree | All levels completely filled  |
| Skewed Tree         | All nodes on one side         |
| Degenerate Tree     | Like linked list              |

#### Difference between Binary tree and Binary search tree

| Feature            | Binary Tree   | Binary Search Tree          |
| ------------------ | ------------- | --------------------------- |
| Max children       | 2             | 2                           |
| Ordering rule      |  No           |  Yes (left < root < right)  |
| Inorder traversal  |  Not sorted   |  Sorted                     |
| Searching          |  Slow (O(n))  |  Faster (O(log n))          |
| Is every BT a BST? |  No           |   —                         |
| Is every BST a BT? |  Yes          |  Yes                        |

### ✅ 4. Complete Binary Tree / Almost Complete Binary Tree (ACBT)

<img width="1478" height="666" alt="image" src="https://github.com/user-attachments/assets/506fbd93-cbbc-4abd-b281-7abea71e948d" />
```
Definition
A Complete Binary Tree is a binary tree where:
All levels are completely filled except possibly last
Last level is filled from left to right
👉 Almost Complete Binary Tree (ACBT) is same definition used in CDAC.

Examples
Used in Heap
Used in Array representation

📌 MCQ Tip:
ACBT does not require last level to be full
Filling must be left to right
```
### 📦 5. Array Implementation of ACBT

- Why Array? : Because ACBT has no gaps
<img width="801" height="401" alt="image" src="https://github.com/user-attachments/assets/9cf2c966-eb8c-4aba-bdf4-2dc3b1aa1f6a" />

| Node at index i | Formula       |
| --------------- | ------------- |
| Left Child      | `2i + 1`      |
| Right Child     | `2i + 2`      |
| Parent          | `(i - 1) / 2` |

```
Advantages
No pointer overhead
Cache friendly

Disadvantage
Wastes space if tree not complete

📌 MCQ Tip:
Array representation is efficient only for ACBT
```
### 🌳 Binary Search Tree (BST)
```
🔹 Definition
A Binary Search Tree (BST) is a binary tree in which every node follows this ordering rule:
Left subtree values < Root
Right subtree values > Root
This rule is true recursively for every node.

🔹 Key Properties (Exam-oriented)
Each node has at most two children
No duplicate values (in standard BST)
Inorder traversal → sorted (ascending) order
Efficient search, insert, delete
```
| Operation | Average Time | Worst Case |
| --------- | ------------ | ---------- |
| Search    | O(log n)     | O(n)       |
| Insert    | O(log n)     | O(n)       |
| Delete    | O(log n)     | O(n)       |
- (Worst case → skewed tree)

```
Important Points
Inorder traversal → sorted sequence
Duplicate keys usually not allowed

📌 MCQ Trap:
- BST can become skewed
- BST is not always balanced

#### 🌳 “BST can become skewed” — what does it mean?
-A Binary Search Tree (BST) is said to be skewed when all nodes are on only one side (left or right), so the tree looks like a linked list instead of a balanced tree.
```
Types of Skewed BST
1️⃣ Right-skewed BST
Happens when elements are inserted in increasing order

10
  \
   20
     \
      30
        \
         40
```

```
2️⃣ Left-skewed BST
Happens when elements are inserted in decreasing order

        40
       /
     30
     /
   20
   /
 10
```

```
Why skewing is bad (Exam Point)
Height of tree = n
Searching becomes O(n) instead of O(log n)
BST loses its main advantage (fast search)
```
| Statement                                 | True / False |
| ----------------------------------------- | ------------ |
| A skewed BST behaves like a linked list   |  True        |
| Inorder traversal of skewed BST is sorted |  True        |
| Skewed BST gives O(log n) search          |  False       |
| Skewing happens due to sorted insertion   |  True        |

### ⚖️ 7. AVL Tree (Adelson-Velsky & Landis Tree)

- What is AVL Tree? : A self-balancing Binary Search Tree
- Balance Factor = Height(left subtree) − Height(right subtree)
- Allowed values: −1, 0, +1

| Case | Rotation       |
| ---- | -------------- |
| LL   | Right rotation |
| RR   | Left rotation  |
| LR   | Left-Right     |
| RL   | Right-Left     |

```
Advantages
Guaranteed O(log n) search time

Disadvantages
Extra rotations
More complex than BST

📌 MCQ Tip:
AVL tree always balanced
Height is always O(log n)
```
```
Q. In array implementation (0-based), parent of node at index 10 is at:
a) 4
b) 5
c) 9
d) 20
Ans: Parent index = (i - 1) / 2
(10 - 1) / 2 = 4.5 → 4 (integer division)
near ans 5.
```
<hr>

## Hashing

### 🔹 Hash Function
👉 A hash function is a function that converts a key into an index (hash value) used to store data in a hash table.
- storing and retriving data from database at a time
- time complexity O(1).
- hash function = k mod 10, k mod n, mid square, folding method

### 🔹 Hash Table
👉 A hash table is a data structure that stores key–value pairs using a hash function.
- Definition (Exam Ready) : A hash table stores data by computing an index from a hash function, enabling fast search, insert, and delete operations.
