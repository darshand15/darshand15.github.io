---
title: "Implementation of Treaps"
collection: projects
---

## Summary

A project aimed at implementing Treap as a generic data structure along with the different functionalities of a treap. Treap is a data structure that stores pairs (say [X,Y]) in a binary tree such that it is a binary search tree by X and a binary heap by Y. In such an implementation, X values are the keys while the Y values are the priorities that specify how the tree is constructed. In this project, the priorities are randomized, thereby using Randomization and the Binary Heap property to construct a randomized balanced binary search tree that maintains balance with high probability. The entire treap and its individual nodes were built as generic canonical classes, thereby supporting all the different data types. The project involved the implementation of multiple operations such as insert node, delete node, split treap, merge two treaps, union, intersection, difference and traversal of treaps. A bidirectional iterator was implemented as a nested class within the treap class. Multiple member algorithms such as find and replace were implemented for treaps. This project was implemented as part of the Generic Programming Course during my Undergraduate Study.

## Implementation Details

The treap data structure and its operations have been implemented as part of header file that the user can include as a library in their client files to invoke and use treap as a generic container. The treap data structure has been implemented using C++ templates to make it a generic container that can support all data types. 

Each node of the treap has been represented as a generic class with the following attributes:
 * Pair of key and priority
 * Pointer to left child of the node
 * Pointer to right child of the node
 * An implementation field to mark a node as a duplicate

This Treap_node class has been made canonical by providing a constructor, a copy constructor, copy assignment operator and a destructor.

The Treap itself has been represented as a generic class with the following attributes:
 * Pointer to the root of the treap
 * An implementation field to decide the way in which the priorities are defined. By default, the priorities are assigned randomly
 * An implementation field to store all the previously defined priorities to ensure that the priorities are not repeated for different nodes.

The Treap class has been made canonical by providing a constructor, a copy constructor, copy assignment operator and a destructor.
Further, a special constructor called the build constructor has been provided that takes in a pair of iterators pointing to a collection of data items and creates a Treap consisting of these data items in linear time. 

### Operations that can be performed on a Treap:

**Insert Node**




Link to video demo, report, readme, ..