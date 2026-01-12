# DSA
Algorithm and Data Structure

## *Design pattern to solve problem in algorithm*
<img width="800" height="533" alt="image" src="https://github.com/user-attachments/assets/3be63d1d-b451-4bd3-b162-af7d40c4e9aa" />

- Dynamic programming always give a optimal path.
- In Dynamic programming - 1)optimal substructure, 2)overlapping subproblems
- In Dynamic programming - stored the subproblem , when repeat this problem no need to calculate it stored already in memory.

- Brute Force technique - “Try everything and pick the correct answer."

- Branch and Bound Algorithm - Branching is the process of generating subproblems. Bounding refers to ignoring partial solution that cannot be better than the current best solution. It is search procedure to find the optimal solution. It eliminates those parts of a search spacewhich does not contain better solution.

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

| Tree Type                              | Condition                                                                  |
| -------------------------------------- | -------------------------------------------------------------------------- |
| **Binary Tree**                        | Each node has **≤ 2 children**.                                            |
| **Strict / Full Binary Tree**          | Every node has **0 or 2 children** only.                                   |
| **Complete Binary Tree (CBT)**         | All levels full except possibly last; last level filled **left to right**. |
| **Almost Complete Binary Tree (ACBT)** | Same as CBT: last level may be partial but **left-aligned**.               |

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
```


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
Complete Binary Trees are always left-biased (last level filled from left).
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

Important Points
- Inorder traversal → sorted sequence
- Duplicate keys usually not allowed

📌 MCQ Trap:
- BST can become skewed
- BST is not always balanced

#### 🌳 “BST can become skewed” — what does it mean?
- A Binary Search Tree (BST) is said to be skewed when all nodes are on only one side (left or right), so the tree looks like a linked list instead of a balanced tree.

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

<hr>

## *Time and Space Complexity*

### *Searching*
| Search Method     | Best Case                      | Average Case | Worst Case                | Space Complexity                                   |
| ----------------- | ------------------------------ | ------------ | ------------------------- | -------------------------------------------------- |
| **Linear Search** | **O(1)** (first element found) | **O(n)**     | **O(n)** (last/not found) | **O(1)**                                           |
| **Binary Search** | **O(1)** (middle element)      | **O(log n)** | **O(log n)**              | **O(1)** (Iterative) <br> **O(log n)** (Recursive) |

- Linear Search works on unsorted or sorted data.
- Binary Search works only on sorted data.

  
### *Sorting*
| Sorting Algorithm  | Best Case                        | Average Case | Worst Case        | Space Complexity                 |
| ------------------ | -------------------------------- | ------------ | ----------------- | -------------------------------- |
| **Selection Sort** | O(n²)                            | O(n²)        | O(n²)             | O(1)                             |
| **Insertion Sort** | O(n) (already sorted)            | O(n²)        | O(n²)             | O(1)                             |
| **Bubble Sort**    | O(n) (optimized, already sorted) | O(n²)        | O(n²)             | O(1)                             |
| **Heap Sort**      | O(n log n)                       | O(n log n)   | O(n log n)        | O(1)                             |
| **Merge Sort**     | O(n log n)                       | O(n log n)   | O(n log n)        | O(n)                             |
| **Quick Sort**     | O(n log n)                       | O(n log n)   | O(n²) (bad pivot) | O(log n) (avg) <br> O(n) (worst) |

- Selection, Insertion, Bubble → Simple but slow (O(n²))
- Heap Sort → Fast and in-place
- Merge Sort → Stable, uses extra memory
- Quick Sort → Fastest on average, worst case O(n²) due to poor pivot choice

### *Hashing & Hash Table – Complexity*
```
Let
n = number of elements
m = size of hash table
α = n / m = load factor
```
| Operation  | Average Time | Worst Time | Space |
| ---------- | ------------ | ---------- | ----- |
| **Search** | O(1)         | O(n)       | O(m)  |
| **Insert** | O(1)         | O(n)       | O(m)  |
| **Delete** | O(1)         | O(n)       | O(m)  |

- Worst case occurs when many keys collide and form a chain/probe sequence
```
Types of Hash Functions (conceptual cost is same):
Division Method
Mid-Square Method
Folding Method
Multiplication Method
All work in O(1) time.
```
#### *Collision Resolution Techniques*

| Technique             | Search / Insert (Average) | Worst Case | Space    |
| --------------------- | ------------------------- | ---------- | -------- |
| **Linear Probing**    | O(1)                      | O(n)       | O(m)     |
| **Quadratic Probing** | O(1)                      | O(n)       | O(m)     |
| **Double Hashing**    | O(1)                      | O(n)       | O(m)     |
| **Chaining**          | O(1)                      | O(n)       | O(m + n) |

```
Linear Probing: h(k), h(k)+1, h(k)+2, ...

Quadratic Probing: h(k) + i²

Double Hashing: h1(k) + i * h2(k)
```

```
Key Exam Points
Hashing gives constant time operations on average.
Poor hash function or high load factor → O(n) worst case.
Open addressing methods (Linear, Quadratic, Double) use no extra list space.
Chaining uses extra memory but reduces clustering.
````

### *📊 Graph Theory – Time & Space Complexity Summary*

```
Let:
V = Number of vertices
E = Number of edges
```

🔷 Graph Representation

| Method               | Time (Operations)                                        | Space        |
| -------------------- | -------------------------------------------------------- | ------------ |
| **Adjacency Matrix** | Edge check: O(1) <br> Traverse neighbors: O(V)           | **O(V²)**    |
| **Adjacency List**   | Edge check: O(deg(V)) <br> Traverse neighbors: O(deg(V)) | **O(V + E)** |


🔷 Graph Traversal Algorithms

| Algorithm | Using Adjacency List | Using Adjacency Matrix | Extra Space |
| --------- | -------------------- | ---------------------- | ----------- |
| **BFS**   | O(V + E)             | O(V²)                  | O(V)        |
| **DFS**   | O(V + E)             | O(V²)                  | O(V)        |


🔷 Shortest Path Algorithms

| Algorithm                             | Purpose                     | Time Complexity                                    | Space Complexity |
| ------------------------------------- | --------------------------- | -------------------------------------------------- | ---------------- |
| **Dijkstra (Level Setting)**          | Single source shortest path | O(V²) (Matrix) <br> O((V + E) log V) (Heap + List) | O(V)             |
| **Floyd–Warshall (Level Correcting)** | All-pairs shortest path     | **O(V³)**                                          | **O(V²)**        |


🔷 Spanning Tree Algorithms (MST)

| Algorithm                | Time Complexity  | Space Complexity |
| ------------------------ | ---------------- | ---------------- |
| **Prim’s (Matrix)**      | O(V²)            | O(V²)            |
| **Prim’s (List + Heap)** | O((V + E) log V) | O(V + E)         |
| **Kruskal’s**            | O(E log E)       | O(V + E)         |

```
📝 Exam-Oriented Points
Matrix → Dense graphs, more space
List → Sparse graphs, less space
BFS / DFS → O(V + E) using list
Dijkstra → Single source
Floyd–Warshall → All pairs
Prim & Kruskal → Greedy MST algorithms
```

### *🌳 Trees – Time & Space Complexity*

🔹 Tree Traversals <br>
(Preorder, Inorder, Postorder, Level Order)

| Operation           | Time Complexity | Space Complexity           |
| ------------------- | --------------- | -------------------------- |
| Traversal           | **O(n)**        | **O(h)** (Recursion/Stack) |
| Level Order (Queue) | **O(n)**        | **O(n)**                   |


🔹 Binary Tree (General)
| Operation | Time | Space |
| --------- | ---- | ----- |
| Search    | O(n) | O(h)  |
| Insert    | O(n) | O(h)  |
| Delete    | O(n) | O(h)  |

- (Because no ordering is guaranteed)

🔹 Complete / Almost Complete Binary Tree (ACBT)
| Operation               | Time     | Space |
| ----------------------- | -------- | ----- |
| Height                  | O(1)     | O(1)  |
| Access by Index (Array) | O(1)     | O(n)  |
| Insert (Heap-like)      | O(log n) | O(n)  |
| Delete                  | O(log n) | O(n)  |

- Stored in array form.
- Parent = (i-1)/2, Left = 2i+1, Right = 2i+2.


🔹 Binary Search Tree (BST)
| Operation | Average Case | Worst Case | Space |
| --------- | ------------ | ---------- | ----- |
| Search    | O(log n)     | O(n)       | O(h)  |
| Insert    | O(log n)     | O(n)       | O(h)  |
| Delete    | O(log n)     | O(n)       | O(h)  |

- Worst case happens when BST becomes skewed.


🔹 AVL Tree (Self-Balancing BST)
| Operation | Time Complexity | Space Complexity |
| --------- | --------------- | ---------------- |
| Search    | **O(log n)**    | O(log n)         |
| Insert    | **O(log n)**    | O(log n)         |
| Delete    | **O(log n)**    | O(log n)         |
| Rotation  | O(1)            | O(1)             |

- AVL tree maintains balance factor = -1, 0, +1.
- Height is always O(log n), so operations never degrade to O(n).

Quick Exam Summary
| Structure    | Search      | Insert   | Delete   | Space    |
| ------------ | ----------- | -------- | -------- | -------- |
| Binary Tree  | O(n)        | O(n)     | O(n)     | O(h)     |
| ACBT (Array) | O(1) access | O(log n) | O(log n) | O(n)     |
| BST (Avg)    | O(log n)    | O(log n) | O(log n) | O(h)     |
| BST (Worst)  | O(n)        | O(n)     | O(n)     | O(n)     |
| AVL Tree     | O(log n)    | O(log n) | O(log n) | O(log n) |


### *Linear Data Structure*
- Let n = number of elements.

| Data Structure                | Operation              | Time Complexity | Space Complexity |
| ----------------------------- | ---------------------- | --------------- | ---------------- |
| **Array**                     | Access (by index)      | **O(1)**        | **O(n)**         |
|                               | Search                 | O(n)            |                  |
|                               | Insert (at end)        | O(1)            |                  |
|                               | Insert/Delete (middle) | O(n)            |                  |
| **Stack** (Array/Linked List) | Push                   | **O(1)**        | **O(n)**         |
|                               | Pop                    | **O(1)**        |                  |
|                               | Peek                   | **O(1)**        |                  |
| **Queue**                     | Enqueue                | **O(1)**        | **O(n)**         |
|                               | Dequeue                | **O(1)**        |                  |
|                               | Front/Rear             | **O(1)**        |                  |
| **Circular Queue**            | Enqueue                | **O(1)**        | **O(n)**         |
|                               | Dequeue                | **O(1)**        |                  |
|                               | Front/Rear             | **O(1)**        |                  |

## Linked List
- Let n = number of nodes in the list.

| Linked List Type         | Operation           | Time Complexity                | Space Complexity                             |
| ------------------------ | ------------------- | ------------------------------ | -------------------------------------------- |
| **Singly Linked List**   | Access / Search     | **O(n)**                       | **O(n)**                                     |
|                          | Insert at Beginning | **O(1)**                       |                                              |
|                          | Insert at End       | O(n) *(O(1) if tail pointer)*  |                                              |
|                          | Delete at Beginning | **O(1)**                       |                                              |
|                          | Delete at End       | O(n)                           |                                              |
| **Doubly Linked List**   | Access / Search     | **O(n)**                       | **O(n)** *(more than SLL due to 2 pointers)* |
|                          | Insert at Beginning | **O(1)**                       |                                              |
|                          | Insert at End       | **O(1)**                       |                                              |
|                          | Delete at Beginning | **O(1)**                       |                                              |
|                          | Delete at End       | **O(1)**                       |                                              |
| **Circular Linked List** | Access / Search     | **O(n)**                       | **O(n)**                                     |
|                          | Insert at Beginning | **O(1)**                       |                                              |
|                          | Insert at End       | **O(1)** *(with tail pointer)* |                                              |
|                          | Delete at Beginning | **O(1)**                       |                                              |
|                          | Delete at End       | O(n) *(O(1) in circular DLL)*  |                                              |

```
Key Points
All linked lists use O(n) space for n nodes.
Doubly linked list uses extra memory per node (prev + next).
Circular lists avoid NULL at the end and are useful in round-robin scheduling.
```

<hr>

###4️⃣ Node-based Storage with Arrays
- Nodes are stored in arrays but linked using indices instead of pointers.
```
Index: 0   1   2
Data:  10  20  30
Next:  1   2  -1

Useful in:
Memory-constrained systems
Simulating linked list without pointers
```
| Feature         | Array          | Linked List         |
| --------------- | -------------- | ------------------- |
| Memory          | Contiguous     | Non-contiguous      |
| Size            | Fixed          | Dynamic             |
| Access          | O(1) random    | O(n) sequential     |
| Insert/Delete   | Costly (shift) | Easy (change links) |
| Cache-friendly  | Yes            | No                  |
| Memory Overhead | Low            | Extra pointer(s)    | 
```

🧠 Memory Allocation in Recursion
Each recursive call gets:
Its own stack frame

Separate copies of:
Parameters
Local variables
Return address
All calls are stored in the call stack.
```
| Recursive Function             | Recurrence             | Time Complexity |
| ------------------------------ | ---------------------- | --------------- |
| `fact(n) = fact(n-1)`          | T(n) = T(n−1) + c      | **O(n)**        |
| `fib(n) = fib(n-1) + fib(n-2)` | T(n) = T(n−1) + T(n−2) | **O(2ⁿ)**       |
| Binary Search                  | T(n) = T(n/2) + c      | **O(log n)**    |
| Merge Sort                     | T(n) = 2T(n/2) + n     | **O(n log n)**  |

<hr>

## 🔐 Hashing & Hash Tables
- Hashing is a technique used to map data (keys) to a fixed-size value called a hash code using a hash function.
- A Hash Table is a data structure that stores data in the form of key–value pairs using hashing for fast access.

Advantages:
- Very fast search, insert, delete
- Average time complexity: O(1)

### 📊 Load Factor in Hashing

- The Load Factor (α) of a hash table is the ratio of the number of stored elements to the total number of slots in the table.

- 𝛼 = Number of keys stored / Size of hash table
```
Example:
If a hash table has 20 slots and 10 keys are stored:

𝛼 = 10/20 = 0.5

🔑 Important Points about Load Factor
Measures fullness of the table
α = 0 → table is empty
α = 1 → table is full

Affects performance
Lower α → fewer collisions → faster operations
Higher α → more collisions → slower search/insert

In Open Addressing
α must be < 1
As α approaches 1, performance degrades rapidly

Typical safe value: 0.5 – 0.7

In Chaining
α can be > 1 (multiple elements per bucket)
Average search time ≈ O(1 + α)

Controls Rehashing
When α exceeds a threshold (e.g., 0.7), the table is resized and rehashing is done.
This maintains efficiency.

Relation with Collisions
Higher load factor ⇒ more collisions
Lower load factor ⇒ better distribution and speed
```

<hr>

### BFS (Breadth First Traversal)
- FT stands for Breadth First Traversal (also called Level Order Traversal).

- In BFT, nodes of a tree are visited level by level, from left to right.
```
Example Binary Tree:

      A
     / \
    B   C
   / \   \
  D   E   F


BFT Output:

A  B  C  D  E  F
```

*Characteristics*
- Visits all nodes at the same depth before moving to next level
- Uses a Queue internally
- Also called Level Order Traversal

*Used in*
- Finding shortest path in trees
- Checking if a tree is complete
- Printing tree level-wise


<hr>

## AVL Tree
- AVL Tree is named after its inventors Georgy Adelson-Velsky and Evgenii Landis.
- An AVL Tree is a self-balancing Binary Search Tree (BST) where the height difference (balance factor) between left and right subtrees of any node is at most 1.
- This keeps operations efficient:
```
Search → O(log n)
Insert → O(log n)
Delete → O(log n)
```

| Case | Rotation              |
| ---- | --------------------- |
| LL   | Right Rotation        |
| RR   | Left Rotation         |
| LR   | Left → Right Rotation |
| RL   | Right → Left Rotation |

<hr>

## Graph
Complete Graph Formula
```
For a complete graph with `n` vertices:
- Number of edges:
E = n(n - 1) / 2

- Number of spanning trees (Cayley’s Formula):
T = n^(n - 2)

So, a complete graph `K_n` has `n^(n - 2)` different spanning trees.

```

| Point           | Dijkstra’s Algorithm                                    | Floyd–Warshall Algorithm                          |
| --------------- | ------------------------------------------------------- | ------------------------------------------------- |
| Type            | Single-source shortest path                             | All-pairs shortest paths                          |
| Finds           | Shortest path from **one source** to all other vertices | Shortest paths between **every pair** of vertices |
| Approach        | Greedy                                                  | Dynamic Programming                               |
| Time Complexity | `O(V²)` (or `O(E log V)` with heap)                     | `O(V³)`                                           |
| Best For        | Large graphs with one starting node                     | Small or medium graphs where all paths are needed |
| Edge Weights    | Works with non-negative weights only                    | Works with negative weights (no negative cycle)   |
| Use Case        | GPS, routing from one point                             | Network analysis, distance matrix                 |



