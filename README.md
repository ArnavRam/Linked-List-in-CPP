# Experiment 17 - Implementation of Linked Lists in C++

---

## Aim
- To study and implement **Linked List** operations in C++, including node creation, insertion, and traversal.
- To understand how linked lists differ from arrays in terms of memory allocation, flexibility, and efficiency.

---

## Tools Used
- Visual Studio Code
- MinGW-w64 with g++ Compiler

---

## Theory
A **Linked List** is a dynamic data structure that stores elements (called **nodes**) in non-contiguous memory locations. Unlike arrays, which require a fixed size, linked lists can grow and shrink at runtime.

Each **node** in a linked list consists of two parts:
1.  **Data field:** Stores the actual value.
2.  **Pointer (`next`):** Stores the memory address of the next node in the sequence.

The **head pointer** always points to the first node of the list. If the list is empty, `head = NULL`. Traversal begins from the head and continues until a node's `next` pointer is `NULL`, which signifies the end of the list.

### Key Characteristics
- **Dynamic Size:** Can grow or shrink during execution.
- **Efficient Insertions/Deletions:** No shifting of elements is required, unlike arrays.
- **Sequential Access:** Elements must be accessed in order from the head. Random access is not possible.

### Types of Linked Lists
- **Singly Linked List:** Each node points only to the next node.
- **Doubly Linked List:** Each node points to both the next and previous nodes.
- **Circular Linked List:** The last node points back to the first node.

---

## Algorithm / Logic

### Program 1: Single Node Creation
1.  **Start**
2.  Define a `Node` structure or class with two fields: `data` (e.g., an integer) and `next` (a pointer to a `Node`).
3.  In `main()`, create a new node dynamically using `new Node()`.
4.  Assign a value to the node's `data` field.
5.  Initialize its `next` pointer to `NULL`.
6.  Display the node’s data to confirm its creation.
7.  **End**

### Program 2: Multiple Nodes & Traversal
1.  **Start**
2.  Define the `Node` structure as in the previous program.
3.  Create multiple nodes dynamically (e.g., `head`, `second`, `third`).
4.  Link them sequentially: `head->next = second;`, `second->next = third;`.
5.  Set the `next` pointer of the last node to `NULL`: `third->next = NULL;`.
6.  Initialize a temporary pointer `temp = head`.
7.  Use a `while` loop that continues as long as `temp != NULL`.
8.  Inside the loop, print `temp->data` and then move to the next node: `temp = temp->next;`.
9.  **End**

### Program 3: Insertion at the Head
1.  **Start**
2.  Define the `Node` structure and a global `head` pointer, initialized to `NULL`.
3.  Create a function `insertAtHead(int value)`.
4.  Inside the function, create a new node.
5.  Assign the `value` to the new node's `data`.
6.  Set the new node's `next` pointer to the current `head`: `new_node->next = head;`.
7.  Update the `head` to point to the new node: `head = new_node;`.
8.  In `main()`, call this function multiple times to add elements to the list.
9.  Traverse the list from the final `head` to display the updated sequence.
10. **End**

---

## Conclusion
Linked lists are a powerful and flexible alternative to arrays, offering efficient memory usage and dynamic growth. This experiment demonstrated the fundamental operations: creating a single node, linking multiple nodes, and inserting new nodes at the head of the list. These operations form the foundation for more advanced manipulations such as deletion, searching, and reversal. Mastering linked lists is essential for understanding higher-level data structures like stacks, queues, and graphs.
