---
layout: post
title: "Linked Lists: Understanding the Basics"
date: 2025-05-13 16:42:56 +0300
categories: Data Structures and Algorithms
---

Welcome to my coding journey! This marks the first entry in what I hope becomes a valuable repository of knowledge—both for myself and perhaps for fellow developers out there walking similar paths.

## My DSA Learning Journey

I've decided to delve into DSA (Data Structures and Algorithms) knowledge to become a better software developer. DSA is a foundational area in computer science that focuses on how data is organized (data structures) and the methods used to process that data efficiently (algorithms).

After watching a few YouTube videos from various people, I realized I was gaining some familiarity but needed to learn from one consistent source, so I took a Udemy course. At this point, I've finished learning about Big O notation and Linked Lists.

## Arrays vs. Linked Lists

Unlike arrays which have indexes, linked lists rely on references. Arrays store elements in contiguous memory locations, while linked lists can have elements scattered throughout memory.

A linked list has both a head and a tail. Each item in the linked list points to the next item, except for the last one which points to null.

<!-- ![Linked List Structure](/assets/images/linked-list-diagram.png) -->

## Time Complexity Operations

When working with linked lists, different operations have different time complexities:

| Operation | Time Complexity | Description |
|-----------|----------------|-------------|
| Adding to end | O(1) | We simply set the tail to point to the new element |
| Removing from end | O(n) | We need to traverse the entire list from the head to find the second-to-last element, then set it as the new tail |
| Adding to beginning | O(1) | We create a pointer from the new element to the current head, then set the head to the new element |
| Removing from beginning | O(1) | Similar to adding - we point the head to the second element and remove the previous head |

## Inserting and Removing from the Middle

To insert an element at the middle (for example, at index 3):

1. We start from the head and traverse to index 3
2. Make the new element point to where the element at index 3 is pointing
3. Make the element at index 3 point to our new element

Since we traversed the list from the head, this operation is O(n).

Similarly, for removing an element from the middle (say index 3):

1. Start from the head and traverse to find the element
2. Make the previous element point to the element after the one we're removing
3. Remove the element

This is also O(n) since we need to traverse the list.

{% highlight javascript %}
// Example code: Inserting a node at position 3
function insertAtPosition(position, value) {
  // Create new node
  const newNode = { value: value, next: null };
  
  // If empty list or position is 0
  if (!this.head || position === 0) {
    newNode.next = this.head;
    this.head = newNode;
    if (!this.tail) this.tail = newNode;
    return;
  }
  
  // Find the node just before the insertion point
  let current = this.head;
  let index = 0;
  while (current && index < position - 1) {
    current = current.next;
    index++;
  }
  
  // Insert the node
  if (current) {
    newNode.next = current.next;
    current.next = newNode;
    
    // If we're at the end, update tail
    if (!newNode.next) this.tail = newNode;
  }
}
{% endhighlight %}

## Arrays vs. Linked Lists - When to Use Which

There's a pattern here that helps us decide which data structure to use:

- For operations like pop() and push() (end operations), arrays are more efficient with O(1) while linked lists are O(n) for pop
- For operations like shift() and unshift() (beginning operations), linked lists are more efficient with O(1) while arrays are O(n)

This makes linked lists particularly useful when you need frequent insertions or deletions at the beginning of your data structure.

## Summary

| Operation | Array | Linked List |
|-----------|-------|-------------|
| Access by index | O(1) | O(n) |
| Insert/remove at beginning | O(n) | O(1) |
| Insert/remove at end | O(1) | O(1)/O(n) |
| Insert/remove in middle | O(n) | O(n) |
| Memory allocation | Contiguous | Scattered |

