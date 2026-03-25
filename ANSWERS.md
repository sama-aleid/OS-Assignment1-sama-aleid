# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
A process is an independent program in execution that has its own memore space recources and system state, a thread is a smaller unit of execution within a process that shares the same memore and resources with other threads in the same process.

in this assignment we used threads because threads are more efficcient for simulations like CPU scheduling and its easier and faster.
---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

in  Round-Robin scheduling if a process does not finish within its assigned time quantum its paused and moved to the end of the ready queue

Example from my output:
``` ? P1 executing quantum [4000ms] 
  ? Quantum progress: [???????????????] 100%
  ? P1 completed quantum 4000ms ? Overall progress: [????????????????????] 45%
     Remaining time: 4866ms
  ? P1 yields CPU for context switch

  ? P1 added to ready queue|
  
```

**Explanation of example:**
in this example process p1 did not finish execution within the time quantum of 4000ms its was paused since it still had remaining time it was added back to the ready queue whin its turn comes again it will resume execution from where it stopped

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**


1. **New**:p1 is in the new state whin it is first created using the constructor byt before calling start().

2. **Runnable**:p1 becomes runnable after calling start() meaning it is ready to run and waiting for CPU scheduling

3. **Running**:p1 enters the running state when the CPU assigns it time to excuete its quantum using the run() method 

4. **Waiting**:p1 goes into the waiting state when it is paused after finish its time quantum or during thread.sleep() while simulating execution

5. **Terminated**:p1 reaches the terminated state when its remaining time becomes zero and it finishes execution completely

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: operating system task scheduling 

**Description**: 
 operating system use scheduling algorithms to manage multiple running applications such as browsers media players

**Why Round-Robin works well here**: 
 Round-Robin ensures that each process gets equal CPU time which improves fairness and responsiveness

### Example 2: web servers handling multiple requests

**Description**: 
 web servers handle multiple client requests simultaneously such as loading web pages or processing API calls

**Why Round-Robin works well here**: 

 Round-Robin allows each request to be processed for a short time before moving to the next ensuring that all clients are served fairly this improve response time and prevents long request from blocking others
---

## Summary

**Key concepts I understood through these questions:**
1. difference between threads and processes
2.how Round-Robin scheduling ensures fairness 
3. the life cycle of a thread and its states

**Concepts I need to study more:**
1. advanced scheduling algorithms
2. threads synchronization 
