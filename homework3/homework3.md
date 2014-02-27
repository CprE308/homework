# Homework 3
> CprE 308, Spring 2014

**It is not required to hand in this homework.**

The problem pointers refer to the class text "Modern Operating Systems" by Tanenbaum, Third Edition, which covers Chapter 6.

1. Students working at individual PCs in a computer laboratory send their files to be printed by a server which spools the files on its hard disk. Under what conditions may a deadlock occur if the disk space for the print spool is limited? How may the deadlock be avoided? (Book Problem 6.2, pg 463)

2. In Fig. 6-1 the resources are returned in the reverse order of their acquisition. Would giving them back in the other order be just as good? (Book Problem 6.3, pg 463)

3. Fig. 6-3 shows the concept of a resource graph. Do illegal graphs exist, that is, graphs that structurally violate the model we have used of resource usage? If so, give an example of one. (Book Problem 6.5, pg 463)

4. Suppose that there is a resource deadlock in a system. Give an example to show that the set of processes deadlocked can include processes that are not in the circular chain in the corresponding resource allocation graph. (Book Problem 6.6, pg 463)

5. Suppose that in Fig. 6-6 $C_{ij} + R_{ij} > E_j$ for some $i$. What implications does this have for the system? (Book Problem 6.9, pg 463)

6. Can a system be in a state that is neither deadlocked nor safe? If so, give an example. If not, prove that all states are either deadlocked or safe. (Book Problem 6.13, pg 464)

7. Consider a system that uses the banker's algorithm to avoid deadlocks. At some time a process *P* requests a resource *R*, but is denied even though *R* is currently available. Does it mean that if the system allocated *R* to *P*, the system would deadlock? (Book Problem 6.14, pg 464)

8. A system has two processes and three identical resources. Each process needs a maximum of two resources. Is deadlock possible? Explain your answer. (Book Problem 6.17, pg 464)

9. Consider the previous problem again, but now with *p* processes each needing a maximum of *m* resources and a total of *r* resources available. What conditions must hold to make the system deadlock free? (Book Problem 6.18, pg 464)

10. A computer has six tape drives, with *n* processes competing for them. Each process may need two drives. For what values of *n* is the system deadlock free? (Book Problem 20, pg 464)

11. The banker's algorithm is being run in a system with *m* resource classes and *n* processes. In the limit of large *m* and *n*, the number of operations that must be performed to check a state for safety is proportional to $m^an^b$. What are the values of *a* and *b*? (Book Problem 21, pg 464)

12. A system has four processes and five allocatable resources. The current allocation and maximum needs are as follows:

|          | *Allocated* | *Maximum* | *Available* |
|----------|-------------|-----------|-------------|
|Process A | 1 0 2 1 1   | 1 1 2 1 3 | 0 0 *x* 1 1 |
|Process B | 2 0 1 1 0   | 2 2 2 1 0 |             |
|Process C | 1 1 0 1 0   | 2 1 3 1 0 |             |
|Process D | 1 1 1 1 0   | 1 1 2 2 1 |             |

> What is the smallest value of *x* for which this is a safe state? (Book Problem 6.22, pg 464)

13. Two processes, *A* and *B*, each need three records, 1, 2, and 3, in a database. If *A* asks for them in the order 1, 2, 3, and *B* asks for them in the same order, deadlock is not possible. However, if *B* asks for them in the order 3, 2, 1, then deadlock is possible. With three resources, there are 3! or six possible permutations each process can request the resources. What fraction of all the combinations is guaranteed to be deadlock free? (Book Problem 6.24, pg 464)

14. In an electronic funds transfer system, there are hundreds of identical processes that work as follows. Each process reads an input line specifying an amount of money, the account to be credited, and the account to be debited. Then it locks both accounts and transfers the money, releasing the locks when done. With many processes running in parallel, there is a very real danger that having locked account *x* it will be unable to lock *y* because *y* has been locked by a process now waiting for *x*. Devise a scheme that avoids deadlocks. Do not release an account record until you have completed the transactions. (In other words, solutions that lock one account then release it immediately if the other is locked are not allowed.) (Book Problem 6.26, pg 465)

15. A computer science student assigned to work on deadlocks thinks of the following brilliant way to eliminate deadlocks. When a process requests a resource, it specifies a time limit. If the process blocks because the resource is not available, a timer is started. If the time limit is exceeded, the process is released and allowed to run again. If you were a professor, what grade would you give this proposal and why. (Book Problem 6.28, pg 465)

16. Cinderella and the Prince are getting divorced. To divide their property, they have agreed on the following algorithm. Every morning, each one may send a letter to the other's lawyer requesting one item of property. Since it takes a day for letters to be delivered, they have agreed that if both discover they have requested the same item on the same day, the next day they will send a letter canceling the request. Among their property is their dog, Woofer, Woofer's doghouse, their canary, Tweeter, and Tweeter's cage. The animals love their houses, so it has been agreed that any division of property separating an animal from its house is invalid, requiring the whole division to start over from scratch. Both Cinderella and the Prince desperately want Woofer. So they can go on (separate) vacations, each spouse has programmed a personal computer to handle the negotiation. When they come back from vacation, the computers are still negotiating. Why? Is deadlock possible? Is starvation possible? Discuss. (Book Problem 6.30, pg 465)
