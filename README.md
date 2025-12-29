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
<br>
```
-Eg. infix = A*(B+C)*D <br>
 Postfix - ABC +* D
first to solve parenthesis and then solve multiply in left side then right side.
-EG. x-y*z to prefix and postfix?
1.prefix = -x*yz
2.postfix - xyz*-
```







