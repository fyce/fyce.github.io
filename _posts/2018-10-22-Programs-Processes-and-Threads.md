---
layout: post
title: Programs, Processes & Threads
---

**Programs**

A program is a list of instructions usually stored in a file (usually called an executable e.g. an elf file) stored on some memory device (e.g. a disk) that can be executed by a computer. 

**Process**

A process is an instance of execution of a program. There can be multiple instances of a program, each one of which is a process e.g. multiple instances of your PC calculator program running at any one time.

A process describes a program loaded into computer memory along with all the resources it needs to run/execute e.g. registers, a program counter, a stack and a heap. 
Each process has a seperate memory address space and is usually independent of other processes. This explains why your text processing program can freeze while other programs on your PC are functional.

[![A Process](https://www.backblaze.com/blog/wp-content/uploads/2017/08/diagram-thread-codestack.png)](https://www.backblaze.com/blog/whats-the-diff-programs-processes-and-threads/)

**Threads**

A thread is a unit/sequence of execution within a process. Processes can have multiple threads working on different tasks at (almost) the same time. Threads within a process can share memory and resources.
Each thread has it's own registers and stack but the heap is shared. Threads can communicate with each other easily (due to the shared address space) but problems with one thread affect all threads and the process as a whole.

[![Threads](https://www.backblaze.com/blog/wp-content/uploads/2017/08/diagram-threads.png)](https://www.backblaze.com/blog/whats-the-diff-programs-processes-and-threads/)

Culled from: 
- [Threads vs. Processes: A Look at How They Work Within Your Program](https://www.backblaze.com/blog/wp-content/uploads/2017/08/diagram-thread-codestack.png)
- [What is a "thread" really ?](https://stackoverflow.com/questions/5201852/what-is-a-thread-really)



