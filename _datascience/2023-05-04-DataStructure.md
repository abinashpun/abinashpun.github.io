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


# Linked List