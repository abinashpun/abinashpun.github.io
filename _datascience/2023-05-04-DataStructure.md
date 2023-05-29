---
title: "Data Structure"
excerpt: "Notes on Data Structure"
collection: datascience
---
# Array
- A set of an index and value pairs.
- One of the oldest, most commonly used data structures.
- Locate consecutively in memory, following the order of index (sequential).
- The size of the interval between two consecutive elements is equal to the size of the data type of the element.
- Linear arrays, or one dimensional arrays, are the most basic.
    - Are static in size, meaning that they are declared with a fixed size.
- Dynamic arrays are like one dimensional arrays, but have reserved space for additional elements.
    - If a dynamic array is full, it copies its contents to a larger array.

- **Pros**
    - Simple deployment.
    - Fast access to data of any position using its index.
- **Cons**
    - Deletion, insertion of an element is inefficient: requires copy and paste of the entire subsequent elements.

- **Time Complexity**
    - Indexing: Linear array: O(1), Dynamic array: O(1)
    - Search: Linear array: O(n), Dynamic array: O(n)
    - Optimized Search: Linear array: O(log n), Dynamic array: O(log n)
    - Insertion: Linear array: n/a, Dynamic array: O(n)

<hr>

# Linked List

## Composition

- Head: Beginning of a list. 
- Node: Data + A pointer (link)
    - The pointer contains the address of the next node.
- Tail: End of a list. 

**Pros**
- No memory waste from dynamic allocation.
- Designed to optimize insertion and deletion. Insertion and deletion can be done anywhere and cost less (O(1) to insert in front of the head than arrays (O(n)).

**Cons**
- Complicated implementation.
- Fragmented memory allocation.
- Extra space than array for pointers.
- No direct access to an element in the middle.
- Traverse only one direction, from head to tail.

**Time Complexity**
- Indexing: Linked Lists: O(n)
- Search: Linked Lists: O(n)
- Optimized Search: Linked Lists: O(n)
- Append: Linked Lists: O(1)
- Prepend: Linked Lists: O(1)
- Insertion: Linked Lists: O(n)

## Variations 

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


