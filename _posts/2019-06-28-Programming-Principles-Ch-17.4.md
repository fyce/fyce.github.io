---
layout: post
title: Programming Principles and Practice using C++, Chapter 17.4 - Free Store & Pointers
---

When you start a C++ program, the compiler sets aside memory for:
- code (*code/text storage*)
- global (and static) variables you define (*static storage*)
- memory to be used when functions are called - they need space for their arguments, local variables, callee (return) address etc. (*stack/automatic storage*)

The rest of the computer's memory is available for other uses; it's "free".
This "free store" (*heap*) is available through the keyword *new*.

This is one perspective/model of computer memory. There's other models that for example yield categories like RAM/ROM based on the persistence of memory, speed of access (read/write) etc.

**new**
- requests memory allocation in the heap
- if request successful, returns a pointer holding the start address of the allocated memory
- else returns nullptr
