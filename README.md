# Queue Implementation  

**Name:** Ninad Phatak  
**PRN:** 24070123065  
**Batch:** ENTC A3  

---

## Overview  

A **Queue** is a linear data structure where elements are inserted from one end (rear) and removed from the other end (front).  
It is widely used in task scheduling, buffering, and resource management.  

In C++, a queue can be implemented using arrays, pointers, or the STL `queue` class.  
Here, the queue is implemented using a **static array** with fixed size.  

Key operations in a queue:  
- **Enqueue (Insertion):** Add an element at the rear.  
- **Dequeue (Deletion):** Remove an element from the front.  
- **Display:** Print all elements from front to rear.  
- **Overflow:** When the queue is full and no more elements can be added.  
- **Underflow:** When the queue is empty and no elements can be removed.  

---

## Code 1: Add, Delete Members in Queue & Check Overflow/Empty  

### Algorithm  
1. Initialize a queue with `front = -1` and `rear = -1`.  
2. **Enqueue operation:**  
   - If `rear == SIZE-1`, print **Queue Overflow**.  
   - If `front == -1`, set `front = 0`.  
   - Increment `rear` and insert the new element.  
3. **Dequeue operation:**  
   - If `front == -1` or `front > rear`, print **Queue Underflow**.  
   - Otherwise, remove the element at `front` and increment `front`.  
4. **Display operation:**  
   - If the queue is empty, print **Queue is empty**.  
   - Otherwise, traverse from `front` to `rear` and print all elements.  
5. Continue operations as required.  

### Theory  
This program demonstrates the basic queue operations using an array:  
- **Insertion (Enqueue):** Adds elements sequentially at the rear.  
- **Deletion (Dequeue):** Removes elements from the front.  
- **Overflow check:** Ensures elements cannot be added when the array is full.  
- **Underflow check:** Ensures elements cannot be deleted when the queue is empty.  

Thus, the program simulates the behavior of a simple **static queue**.  

### Output  
10 Inserted into queue.

20 Inserted into queue.

30 Inserted into queue.

Queue elements:10 20 30

10 Removed from queue.

Queue elements:20 30

40 Inserted into queue.

Queue elements:20 30 40

50 Inserted into queue.

Queue Overflow!
Queue Overflow!
Queue elements:20 30 40 50

yaml
Copy code
