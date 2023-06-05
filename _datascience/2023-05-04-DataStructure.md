---
title: "Data Structure"
excerpt: "Notes on Data Structure"
collection: datascience
---
# Array
- A set of an index and value pairs. One of the oldest, most commonly used data structures.
- Locate consecutively in memory, following the order of index (sequential).
- The size of the interval between two consecutive elements is equal to the size of the data type of the element.
- Linear arrays, or one dimensional arrays, are the most basic.
    - Are static in size i.e., that they are declared with a fixed size.
- Dynamic arrays are like one dimensional arrays but have reserved space for additional elements.
    - If a dynamic array is full, it copies its contents to a larger array.

## Pros
- Simple deployment.
- Fast access to data of any position using its index.

## Cons
- Deletion, insertion of an element is inefficient: requires copy and paste of the entire subsequent elements.

## Time Complexity

- Indexing: Linear array: `O(1)`, Dynamic array: `O(1)`
- Search: Linear array: `O(n)`, Dynamic array: `O(n)`
- Optimized Search: Linear array: `O(log n)`, Dynamic array: ``O(log n)``
- Insertion: Linear array: N/A, Dynamic array: `O(n)`

<hr>

# Linked List

## Composition

- **Head**: Beginning of a list. 
- **Node**: Data + A pointer (link)
    - The pointer contains the address of the next node.
- **Tail**: End of a list. 

## Pros
- No memory waste from dynamic allocation.
- Designed to optimize insertion and deletion. Insertion and deletion can be done anywhere and cost less (`O(1)` to insert in front of the head than arrays `(O(n)`).

## Cons
- Complicated implementation.
- Fragmented memory allocation.
- Extra space than array for pointers.
- No direct access to an element in the middle.
- Traverse only one direction, from head to tail.

## Time Complexity
- Indexing: Linked Lists: ``O(n)``
- Search: Linked Lists: ``O(n)``
- Optimized Search: Linked Lists: ``O(n)``
- Append: Linked Lists: ``O(1)``
- Prepend: Linked Lists: ``O(1)``
- Insertion: Linked Lists: ``O(n)``

## Variations of Linked Lists

### Circular Linked List
- Same structure, except the last node points the first node.
- Traverse to the previous node is possible (on the next round).
- The head pointer is not necessary (head can be replaced by tail.link)

### Double Linked List
- Components:
    - Head: Beginning of a list. 
    - Node: Data + A pointer to the previous node + A pointer to the next node.
    - Tail: End of a list. 
- Can traverse bidirection.
    - Insertion and deletion of a node in front of a given node can be done fast.
- Requires more space for the previous pointers.


<hr>

# Stack, Queue

Stack, Queue, and Deque are commonly used **linear (ordered) data strucrues**. They vary depending on the position of insertion and deletion operation. These are commonly implemented with linked lists but can be made from arrays too.

## Stack
- Insertion and deletion can be done only at the top.
- **LIFO**: Last-In First-Out
- Basic operations
    - **Push**: insert/stack the new element on the top
    - **Pop**: remove the last (top) element
- Stack overflow: push an item when the stack is full.

The implementation is here in the[link](https://github.com/abinashpun/DataScience_Notes/blob/main/DS_Algo_implementation.ipynb).

### Applications of Stack
- Function call
- Recursive function
- **Parenthesis matching**
- Full subway


## Queue
- Insertion (deletion) can be done only at the rear (front).
- **FIFO**: First-In First-Out
- Basic operations
    - Enqueue: insert the new element at the end of a queue
    - Dequeue: remove the oldest element
    - Enqueue and dequeue occur at the opposit sides
- Stack overflow: push an item when the stack is full.


### Application of Queue 
- **OS job scheduling**
- Public bathroom

## Deque
Deque is double ended queue, like Stack+Queue.
Enqueue and Dequeue can be done in both ends.
Python provides a library of deque.

``
from collections import deque 
``

<hr>

# Tree
A tree is a data structure that represents a hierarchical relationship. 
A link to another node is one way (only from higher to lower, no cyclic connection), 
and each node has its own subtree.

### Component
- Node: an element of a tree (data + link to its child node(s))
    - Root node: The top node of a tree
    - Parent node (higher) &harr; Child node (lower)
    - Sibling nodes: Nodes that have the same parent nodes. 
    - Ancestor node: A parent or higher node
    - Descendent node: A child or lower node
    - Terminal node (=leaf): A node that doesn't have a child node
    - Internal node: A node that is not a terminal node
- Edge: a line connects two adjacent nodes

### Terms
- Level: Depth from the root (level of the root = 1)
- Height (=depth of a tree): The maximum level of a tree
- Degree of a node: Its number of child node(s)
- Degree of a tree: The maximum degree of a node within a tree

## Binary tree
A tree whose degree is two or smaller is a binary tree. 
In a binary tree, every internal node has either one or two children. 
Every subtree of a binary tree is another binary tree.

### Points to know
- Designed to **optimize searching and sorting**.
- A degenerate tree is an unbalanced tree, which if entirely one-sided, is essentially a linked list.
- They are comparably simple to implement than other data structures.

### Time complexity
- Indexing: Binary Search Tree: ``O(log n)``
- Search: Binary Search Tree: ``O(log n)``
- Insertion: Binary Search Tree: ``O(log n)``

### N-degree tree can be a binary tree
Every n-degree tree can be transformed into a binary tree by following steps.
1. Remove all edges except the connection between a parent and the most left child.
2. From every node, draw an edge to its sibling at the right. 
3. Rotate the tree 90 degrees clockwise.

### Variations
- Complete binary tree: All internal nodes have two children nodes
- Perfect/Full binary tree: All level is full (l$^{th}$ level has $2^l$ nodes). A perfect binary tree is a complete binary, but not vice versa. 
- Skewed binary tree: Every node has either one or zero child.

The implementation of tree is shown here [here](https://github.com/abinashpun/DataScience_Notes/blob/main/DS_Algo_implementation.ipynb)

<hr>

# Heap
A heap is a complete binary tree, 
where every parent has a key either greater than or equal to (**max heap**) or less than or equal to (**min heap**) its child's key. 

## Properties
- Height of a heap with n nodes: ``log2(n)+1``
- Except for the last level, i-th level has $2^{(i-1)}$ nodes.
- Left child's index = parent's index * 2  
- Right child's index = parent's index * 2 + 1
- Parent's index = Child's index/2

## Insertion (upheap)
1. Insert the new element next to the last node
2. Keep exchanging with its parent until it satisfies max/min heap condition

Time complexity: height of a heap, ``O(log2(n)) ``

## Deletion (downheap)
1. Move the last element to the deleted node
2. Keep exchanging with its larger (smaller) child until it satisfies max (min) heap condition

Time complexity: height of a heap, ``O(log2(n)) ``

## Heap sort
Sorting algorithm which utilize heap structure.
For n elements,
1. Add elements with upheap 
2. Delete and pop element with downheap. Popped element is saved to the sorted array

### Time complexity:
For each element, maximum number of upheap or downheap operation is equal to the tree height, ``O(log2(n))``
Total complexity for n elements: ``O(nlog2(n))``

The implementation is as shown in [here](https://github.com/abinashpun/DataScience_Notes/blob/main/DS_Algo_implementation.ipynb)

<hr>

# Hash Table or Hash Map
## Definition
- A hash table is a data structure that stores **key value pairs**.
- **Hash functions** accept a key and return an output unique only to that specific key.
    - This is known as hashing, which is the concept that an input and an output have a one-to-one correspondence to map information.
    - Hash functions return a unique address in memory for that data.

## What you need to know
- Designed to optimize searching, insertion, and deletion.
- **Hash collisions** are when a hash function returns the same output for two distinct inputs.
    - All hash functions have this problem.
    - This is often accommodated for by having the hash tables be very large.
- Hashes are important for **associative arrays and database indexing**.

## Time Complexity
- Indexing:         Hash Tables: `O(1)`
- Search:           Hash Tables: `O(1)`
- Insertion:        Hash Tables: `O(1)`
