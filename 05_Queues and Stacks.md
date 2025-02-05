# 5. Queues and Stacks

# 5.1. Basics of Stacks

A **stack** is a fundamental data structure that follows the Last-In-First-Out (LIFO) principle - imagine a stack of plates where you can only add or remove from the top.
The main operations on a stack are:

push: adds an element to the top (append in Python lists)
pop: removes and returns the top element (pop in Python lists)
peek/top: views the top element without removing it (stack[-1] in Python)
is_empty: checks if the stack is empty (len(stack) == 0)

A very common approach is just by having a list. 
```
stack = []

# Push operation (adding elements)
stack.append(5)    # stack: [5]
stack.append(10)   # stack: [5, 10]
stack.append(15)   # stack: [5, 10, 15]

# Pop operation (removing elements)
top_element = stack.pop()  # returns 15, stack: [5, 10]
```

# 5.2. Basics of Queues

A **queue** is a First-In-First-Out (FIFO) data structure. Similar to a line of patient samples waiting for genomic sequencing - the first sample submitted is the first one processed.
The main operations on a queue are:

Enqueue: Add element to end (like adding a new patient sample)
Dequeue: Remove first element (like processing the next sample)
Front: View first element without removing it

```
# Queue using a list
sample_queue = []
sample_queue.append("Patient_A_DNA")  # Enqueue
first_sample = sample_queue.pop(0)  # Dequeue
front_sample = sample_queue[0]  # Front
```

We would not dwell too much into stacks and queues as they are not as important for now. 
