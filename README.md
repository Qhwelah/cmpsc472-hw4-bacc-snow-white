# BACC Snow White Storytelling Assignment
## Operating Systems Simultaneous Access Resolution Simulation


## Overview
These programs were written for the BACC program in the language C--

The point of these is to implement programs that would cause bugs or incorrect behaviors as a result of simultaneous access.

BACC simulates simultaneous access with the `cobegin` function.


## Semaphores
Each of these solutions resolves the issue of simultaneous access through the use of **semaphors**, which are essentially global variables that denote when a given variable or "Critical Section" of code is currently being accessed by another process.

In the case that a second program *is* currently accessing that Critical Section, BACC forces the second program to wait for the first to be completed accessing that resource and for it to emit the `signal(semaphor)` command to indicate the resource is now available. 


## Compiling and Running the Code
The `[program-name].cm` files can be compiled by running `bacc [program-name].cm`.

This will generate two files with the same root name: `[program-name].lst` and `[program-name].pco`.

To run the code and see the results, do `bainterp [program-name].pco`. 

Usually, this command is run several times to verify several executions does not reveal some new race condition.