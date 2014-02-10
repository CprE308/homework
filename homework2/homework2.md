# Homework 2
> CprE 308, Spring 2014

**It is not required to turn in this homework.**

 1. In Fig. 2-2, [Process State Diagram with three 3 states] three process states are shown. In theory, with three states, there could be six transitions, two out of each state.  However, only four transitions are shown.  Are there any circumstances in which either or both of the missing transitions might occur? (Book Problem 2.1, pg 170)

 2. On all current computers, at least part of the interrupt handlers are written in assembly language. Why? (Book Problem 2.3, pg 170)

 3. When an interrupt or a system call transfers control to the operating system, a kernel stack area separate from the stack of the interrupted process is generally used.  Why? (Book Problem 2.4, pg 170)

 4. If a multithreaded process forks, a problem occurs if the child gets copies of all the parent's threads.  Suppose that one of the original threads was waiting for keyboard input.  Now two threads are waiting for keyboard input, one in each process.  Does this problem ever occur in single-threaded processes? (Book Problem 2.7, pg 170)

 5. In Fig. 2-8, a multithreaded Web server is shown.  If the only way to read from a file is the normal blocking `read` system call, do you think user-level threads or kernel-level threads are being used for the Web server?  Why? (Book Problem 2.8, pg 170)

 6. In the text, we described a multithreaded Web server, showing why it is better than a single-threaded server and a finite-state machine server.  Are there any circumstances in which a single-threaded server might be better?  Give an example. (Book Problem 2.9, pg 170)

 7. In Fig. 2-12 the register set is listed as a per-thread rather than a per-process item. Why? After all, the machine only has one set of registers. (Book Problem 2.10, pg 170)

 8. Why would a thread ever voluntarily give up the CPU by calling `thread_yield`? After all, since t here is no periodic clock interrupt, it may never get the CPU back. (Book Problem 2.11, pg 170)

 9. Can a thread ever be preempted by a clock interrupt?  If so, under what circumstances? If not, why not? (Book Problem 2.12, pg 170)

 10. In this problem you are to compare reading a file using a single-threaded file server and a multithreaded server.  It takes 15 msec to get a request for work, dispatch it, and do the rest of the necessary processing, assuming that the data needed are in the block cache.  If a disk operation is needed, as is the case one-third of the time, an additional 75 msec is required, during which time the thread sleeps.  How many requests/sec can the server handle if it is single threaded? If it is multithreaded? (Book Problem 2.13, pg 171)

 11. In the discussion on global variables in threads, we used a procedure `create_global` to allocate storage for a pointer to the variable, rather than the variable itself. Is this essential, or could the procedures work with the values themselves just as well? (Book Problem 2.16, pg 171)

 12. Consider a system in which threads are implemented entirely in user space, with the run-time system getting a clock interrupt once a second. Suppose that a clock interrupt occurs while some thread is executing in the run-time system.  What problem might occur?  Can you suggest a way to solve it? (Book Problem 2.17, pg 171)

 13. Does the busy waiting solution using the `turn` variable (Fig. 2-23) work when the two processes are running on a shared-memory multiprocessor, that is, two CPUs sharing a common memory? (Book Problem 2.23, pg 171)

 14. Does Peterson's solution to the mutual exclusion problem shown in Fig. 2-24 work when process scheduling is preemptive?  How about when it is nonpreemptive? (Book Problem 2.24, pg 171)

 15. Give a sketch of how an operating system that can disable interrupts could implement semaphores (Book Problem 2.25, pg 171)

 16. Five batch jobs *A* through *E*, arrive at a computer center at almost the same time.  They have estimated running times of 10, 7, 2, 4, and 8 minutes.  Their (externally determined) priorities are 3, 5, 2, 1, and 4, respectively, with 5 being the highest priority.  For each of the following scheduling algorithms, determine the mean process turn-around time.  Ignore process switching overhead.
    a. Round robin.
    b. Priority scheduling.
    c. First-come, first-served (run in order 10,7,2,4,8).
    d. Shortest job first.

    For (a), assume that the system is multiprogrammed, and that each job gets its fair share of the CPU.  For (b) through (d) assume that only one job at a time runs, until it finishes.  All jobs are completely CPU bound. (Book Problem 2.37, pg 173)

 17. A soft real-time system has four periodic events with periods of 50, 100, 200, and 250 msec each.  Suppose that the four events require 35, 20, 10, and *x* msec of CPU time, respectively.  What is the largest value of *x* for which the system is schedulable? (Book Problem 2.41, pg 173)

 18. A real-time system needs to handle two voice calls that each run every 5 msec and consume 1 msec of CPU time per burst, plus one video at 25 frames/sec, which each frame requiring 20 msec of CPU time.  Is this system schedulable? (Book Problem 2.23, pg 173)

 19. Consider the procedure `put_forks` in Fig. 2-20.  Suppose that the variable `state[i]` was set to `THINKING` *after* the two calls to `test`, rather than *before*.  How would this change affect the solution? (Book Problem 2.46, pg 173)

 20. The readers and writers problem can be formulated in several ways with regard to which category of processes can be started when.  Carefully describe three different variations of the problem, each one favoring (or not favoring) some category of processes.  For each variation, specify what happens when a reader or a writer becomes ready to access the database, and what happens when a process is finished using the database. (Book Problem 2.47, pg 174)
