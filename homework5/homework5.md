# Homework 5
> CprE 308, Spring 2014

**It is not required to hand in this homework.**

The problem pointers refer to the class text "Modern Operating Systems" by Tanenbaum, Third Edition, which covers Chapter 4.

1. A beginning of a free space bitmap looks like this after the disk partition is first formatted: 1000 0000 0000 0000 (the first block is used by the root directory).  The system always searches for free blocks starting at the lowest-numbered block, so after writing file *A*, which uses six blocks, the bitmap looks like this: 1111 1110 0000 0000.  Show the bitmap after each of the following additional actions:

     a. File *B* is written, using five blocks
     b. File *A* is deleted
     c. File *C* is written, using eight blocks
     d. File *B* is deleted (Book Problem 4.20, pg 326)

2. A certain file system uses 2-KB disk blocks.  The median file size is 1 KB.  If all files were exactly 1 KB, what fraction of the disk space would be wasted?  Do you think the wastage for a real file system will be higher than this number or lower than it?  Explain your answer. (Book Problem 4.29, pg 327)

3. A UNIX file system has 1-KB blocks and 4-byte disk addresses.  What is the maximum file size if i-nodes contain 10 direct entries, and one single, double, and triple indirect entry each? (Book Problem 4.32, pg 327)

4. How many disk operations are needed to fetch the i-node for the file `/usr/ast/courses/os/handout.t`?  Assume that the i-node for the root directory is in memory, but nothing else along the path is in memory.  Also assume that all directories fit in one disk block. (Book Problem 4.33, pg 327)

5. In many UNIX systems, the i-nodes are kept at the start of the disk.  An alternative design is to allocate an i-node when a file is created and put the i-node at the start of the first block of the file.  Discuss the pros and cons of this alternative. (Book Problem 4.34, pg 327)

