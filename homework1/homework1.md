# Homework 1
> CprE 308, Spring 2014

**It is not required to turn in this homework.**

 1. Which of the following instructions should be allowed only in kernel mode? (Book Problem 1.7, pg 80)
    a. Disable all interrupts
    b. Read the time-of-day clock.
    c. Set the time-of-day clock
    d. Change the memory map.

 2. What is the maximum depth of the stack (in terms of stack frames - one stack frame per function call) for the following piece of code? Remember to count the first call to main(). 


        int main() { 
            f1(5); 
            return 1; 
        } 

        void f1(int n) { 
            if (n <= 0) 
                return; 
            else 
                f2(n-2); 
        } 

        void f2(int n) { 
            if (n <= 0) 
                return; 
            else 
                f1(n+1); 
        }
 
 3. Give conditions when the following UNIX system calls can fail: 
    - fork() 
    - execv() 
    - waitpid() 


 4. Which of the following instructions should be privileged (i.e. not allowed in the user mode)? 
    - Read the system clock
    - Turn off interrupts 
    - Switch from user to kernel mode 

 5. What is the main difference between a TRAP and an interrupt? 

 6. How many processes are created when the following piece of code is executed?  Draw the process tree for the processes thus created. 

        int main() { 
            int i; 
            for (i=0; i<4; i++) 
                fork(); 
            return 1; 
        } 

 7. When a user program makes a system call to read or write a disk file, it provides an indication of which file it wants, a pointer to the data buffer, and the count.  Control is then transferred to the operating system, which calls the appropriate driver.  Supose that the driver starts the disk and terminates until an interrupt occurs.  In the case of reading from the disk, obviously the caller will have to be blocked (because there are no data for it). What about the case of writing to the disk? Need the caller be blocking awaiting completion of the disk transfer? (Book Problem 1.12, pg 80)

 8. Among all the system calls that you have seen so far, which would you label as providing some sort of *inter* process communication (i.e. between different processes)? 

 9. A file whose file descripter if *fd* cointains the following sequence of bytes: 3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5.  The following system calls are made where the `lseek` call makes a seek to byte 3 of the file.  What does *buffer* cointain after the read has completed?  (Book Problem 1.20, pg 81)

        lseek(fd, 3, SEEK_SET);
        read(fd, &buffer, 4);


