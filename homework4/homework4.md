# Homework 4
> CprE 308, Spring 2014

**It is not required to hand in this homework.**

The problem pointers refer to the class text "Modern Operating Systems" by Tanenbaum, Third Edition, which covers Chapter 3.

1. In this problem you are to compare the storage needed to keep track of free memory using a bitmap versus using a linked list.  The 128-MB memory is allocated in units of *n* bytes.  For the linked list, assume that memory consists of an alternating sequence of segments and holes, each 64 KB.  Also assume that each node in the linked list needs a 32-bit memory address, a 16-bit length, and a 16-bit next-node field.  How many bytes of storage is required for each method?  Which one is better? (Book Problem 3.3, pg 249)

2. Consider a swapping system in which memory consists of the following hole sizes in memory order: 10 KB, 4 KB, 20 KB, 18 KB, 7 KB, 9 KB, 12 KB, and 15 KB.  Which hole is taken for successive segment requests of:
     a. 12 KB
     b. 10 KB
     c. 9 KB

> for first fit?  Now repeat the question for best fit, worst fit, and next fit. (Book Problem 3.4, pg 249)

3. For each of the following decimal virtual addresses, compute the virtual page number and offset for a 4-KB page and for an 8 KB page: 20000, 32758, 60000. (Book Problem 3.5, pg 249)

4. Consider the following C program:

```c
    int X[N];
    int step = M;  // M is some predefined constant
    for (int i = 0; i < N; i += step) X[i] = x[i] + 1;
```

> a. If this program is run on a machine with a 4-KB page size and a 64-entry TLB, what values of M and N will cause a TLB miss for every execution of the inner loop?
> b. Would your answer in part (a) be different if the loop were repeated many times?  Explain. (Book Problem 3.7, pg 249)

5. A machine has a 32-bit address space and an 8-KB page.  The page table is entirely in hardware, with one 32-bit word per entry.  When a process starts, the page table is copied to the hardware from memory, at one word every 100 nsec.  If each process runs for 100 msec (including the time to load the page table), what fraction of the CPU time is devoted to loading the page tables? (Book Problem 3.9, pg 249)

6. A computer with a 32-bit address uses a two-level page table.  Virtual addresses are split into a 9-bit top-level page table field, an 11-bit second-level page table field, and an offset.  How large are the pages and how many are there in the address space? (Book Problem 3.12, pg 250)

7. Suppose that a 32-bit virtual address is broken up into four fields, *a,b,c,* and *d*.  The first three are used for a three-level page table system.  The fourth field, *d*, is the offset.  Does the number of pages depend on the sizes of all four fields?  If not, which ones matter and which ones do not?  (Book Problem 3.13, pg 250)

8. A computer has 32-bit virtual addresses and 4-KB pages.  The program and data together fit in the lowest page (0-4095).  The stack fits in the highest page.  How many entries are needed in the page table if traditional (one-level) paging is used?  How many page entries are needed for two-level paging, with 10 bits in each part? (Book Problem 3.14, pg 250)

9. A computer whose processes have 1024 pages in their address spaces keeps its page tables in memory.  The overhead required for reading a word from the page table is 5 nsec.  To reduce this overhead, the computer has a TLB, which holds 32 (virtual page, physical page frame) pairs, and can do a look up in 1 nsec.  What hit rate is needed to reduce the mean overhead to 2 nsec. (Book Problem 3.15, pg 250)

10. A machine has 48-bit virtual addresses and 32-bit physical addresses.  Pages are 8 KB.  How many entries are needed for the page table? (Book Problem 3.18, pg 250)

11. A student in a compiler design course proposes to the professor a project of writing a compiler that will produce a list of page references that can be used to implement the optimal page replacement algorithm.  Is this possible?  Why or why not?  Is there anything that could be done to improve paging efficiency at run time? (Book Problem 3.20, pg 250)

12. A small computer has four page frames.  At the first clock tick, the *R* bits are 0111 (page 0 is 0, the rest are 1).  At subsequent clock ticks, the values are 1011, 1010, 1101, 0010, 1010, 1100, and 0001.  If the aging algorithm is used with an 8-bit counter, give the values of the four counters after the last tick. (Book Problem 3.24, pg 251)

13. A computer has four page frames.  The time of loading, time of last access, and the *R* and *M* bits for each page are as shown below (the times are in clock ticks):

| Page | Loaded | Last ref. | R | M |
|------|--------|-----------|---|---|
| 0    | 126    | 280       | 1 | 0 |
| 1    | 230    | 265       | 0 | 1 |
| 2    | 140    | 270       | 0 | 0 |
| 3    | 110    | 285       | 1 | 1 |

 a. Which page will NRU replace?
 b. Which page will FIFO replace?
 c. Which page will LRU replace?
 d. Which page will second chance replace? (Book Problem 3.28, pg 251)


