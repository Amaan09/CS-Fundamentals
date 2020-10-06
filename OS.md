## Operating Systems (OS)

**1.  What is Operating System and Its Types (MultiProcessing ,MultiTasking and All)**

An Operating System (OS) is an interface between a computer user and computer hardware. An operating system is a software which performs all the basic tasks like file management, memory management, process management, handling input and output, and controlling peripheral devices such as disk drives and printers.

1. Batch Operating System –

This type of operating system does not interact with the computer directly. There is an operator which takes similar jobs having same requirement and group them into batches. It is the responsibility of operator to sort the jobs with similar needs. Examples of Batch based Operating System: Payroll System, Bank Statements etc.

2. Time-Sharing Operating Systems –

Each task is given some time to execute, so that all the tasks work smoothly. Each user gets time of CPU as they use single system. These systems are also known as Multitasking Systems. The task can be from single user or from different users also. The time that each task gets to execute is called quantum. After this time interval is over OS switches over to next task. Examples of Time-Sharing OSs are: Multics, Unix etc.

3. Distributed Operating System –

These types of operating system is a recent advancement in the world of computer technology and are being widely accepted all-over the world and, that too, with a great pace. Various autonomous interconnected computers communicate each other using a shared communication network. Independent systems possess their own memory unit and CPU. These are referred as loosely coupled systems or distributed systems. These system’s processors differ in size and function. The major benefit of working with these types of operating system is that it is always possible that one user can access the files or software which are not actually present on his system but on some other system connected within this network i.e., remote access is enabled within the devices connected in that network. Examples of Distributed Operating System are- LOCUS etc.

4. Network Operating System –

These systems run on a server and provide the capability to manage data, users, groups, security, applications, and other networking functions. These type of operating systems allow shared access of files, printers, security, applications, and other networking functions over a small private network. One more important aspect of Network Operating Systems is that all the users are well aware of the underlying configuration, of all other users within the network, their individual connections etc. and that’s why these computers are popularly known as tightly coupled systems. Examples of Network Operating System are: Microsoft Windows Server 2003, Microsoft Windows Server 2008, UNIX, Linux, Mac OS X, Novell NetWare, and BSD etc.

5. Real-Time Operating System –
These types of OSs serves the real-time systems. The time interval required to process and respond to inputs is very small. This time interval is called response time. Real-time systems are used when there are time requirements are very strict like missile systems, air traffic control systems, robots etc.

Batch processing

Batch processing is a technique in which an Operating System collects the programs and data together in a batch before processing starts. An operating system does the following activities related to batch processing −

    The OS defines a job which has predefined sequence of commands, programs and data as a single unit.

    The OS keeps a number a jobs in memory and executes them without any manual information.

    Jobs are processed in the order of submission, i.e., first come first served fashion.

    When a job completes its execution, its memory is released and the output for the job gets copied into an output spool for later printing or processing.


Multitasking

Multitasking is when multiple jobs are executed by the CPU simultaneously by switching between them. Switches occur so frequently that the users may interact with each program while it is running. An OS does the following activities related to multitasking −

    The user gives instructions to the operating system or to a program directly, and receives an immediate response.

    The OS handles multitasking in the way that it can handle multiple operations/executes multiple programs at a time.

    Multitasking Operating Systems are also known as Time-sharing systems.

    These Operating Systems were developed to provide interactive use of a computer system at a reasonable cost.

    A time-shared operating system uses the concept of CPU scheduling and multiprogramming to provide each user with a small portion of a time-shared CPU.

    Each user has at least one separate program in memory.

    A program that is loaded into memory and is executing is commonly referred to as a process.

    When a process executes, it typically executes for only a very short time before it either finishes or needs to perform I/O.

    Since interactive I/O typically runs at slower speeds, it may take a long time to complete. During this time, a CPU can be utilized by another process.

    The operating system allows the users to share the computer simultaneously. Since each action or command in a time-shared system tends to be short, only a little CPU time is needed for each user.

    As the system switches CPU rapidly from one user/program to the next, each user is given the impression that he/she has his/her own CPU, whereas actually one CPU is being shared among many users.

Multiprogramming

Sharing the processor, when two or more programs reside in memory at the same time, is referred as multiprogramming. Multiprogramming assumes a single shared processor. Multiprogramming increases CPU utilization by organizing jobs so that the CPU always has one to execute.

An OS does the following activities related to multiprogramming.

    The operating system keeps several jobs in memory at a time.

    This set of jobs is a subset of the jobs kept in the job pool.

    The operating system picks and begins to execute one of the jobs in the memory.

    Multiprogramming operating systems monitor the state of all active programs and system resources using memory management programs to ensures that the CPU is never idle, unless there are no jobs to process.

**2.  Process and Threads in OS , Process State , Process Control Block and Context Switching (Threading is Important Topic)**

**Process**

A process is basically a program in execution. The execution of a process must progress in a sequential fashion.

    A process is defined as an entity which represents the basic unit of work to be implemented in the system.

To put it in simple terms, we write our computer programs in a text file and when we execute this program, it becomes a process which performs all the tasks mentioned in the program.

When a program is loaded into the memory and it becomes a process, it can be divided into four sections ─ stack, heap, text and data. The following image shows a simplified layout of a process inside main memory −
Process Components

1. Stack: The process Stack contains the temporary data such as method/function parameters, return address and local variables.

2. Heap: This is dynamically allocated memory to a process during its run time.

3. Text: This includes the current activity represented by the value of Program Counter and the contents of the processor's registers.

4. Data: This section contains the global and static variables.

**Process Life Cycle**

![image of process](https://www.tutorialspoint.com/operating_system/images/process_state.jpg)

**Start**

This is the initial state when a process is first started/created.

**Ready**

The process is waiting to be assigned to a processor. Ready processes are waiting to have the processor allocated to them by the operating system so that they can run. Process may come into this state after Start state or while running it by but interrupted by the scheduler to assign CPU to some other process.

**Running**

Once the process has been assigned to a processor by the OS scheduler, the process state is set to running and the processor executes its instructions.

**Waiting**

Process moves into the waiting state if it needs to wait for a resource, such as waiting for user input, or waiting for a file to become available.

**Terminated or Exit**

Once the process finishes its execution, or it is terminated by the operating system, it is moved to the terminated state where it waits to be removed from main memory.

**Process Control Block (PCB)**

![image of pcb](https://www.tutorialspoint.com/operating_system/images/pcb.jpg)

A Process Control Block is a data structure maintained by the Operating System for every process. The PCB is identified by an integer process ID (PID).

```
Process State

The current state of the process i.e., whether it is ready, running, waiting, or whatever.

Process privileges

This is required to allow/disallow access to system resources.

Process ID

Unique identification for each of the process in the operating system.

Pointer

A pointer to parent process.

Program Counter

Program Counter is a pointer to the address of the next instruction to be executed for this process.

CPU registers

Various CPU registers where process need to be stored for execution for running state.

CPU Scheduling Information

Process priority and other scheduling information which is required to schedule the process.

Memory management information

This includes the information of page table, memory limits, Segment table depending on memory used by the operating system.

Accounting information

This includes the amount of CPU used for process execution, time limits, execution ID etc.

IO status information

This includes a list of I/O devices allocated to the process.
```

**Context Switching**

A context switch is the mechanism to store and restore the state or context of a CPU in Process Control block so that a process execution can be resumed from the same point at a later time. Using this technique, a context switcher enables multiple processes to share a single CPU. Context switching is an essential part of a multitasking operating system features. When the scheduler switches the CPU from executing one process to execute another, the state from the current running process is stored into the process control block. After this, the state for the process to run next is loaded from its own PCB and used to set the PC, registers, etc. At that point, the second process can start executing.

**Threads**

A thread is a flow of execution through the process code, with its own program counter that keeps track of which instruction to execute next, system registers which hold its current working variables, and a stack which contains the execution history. A thread is also called a lightweight process. Threads provide a way to improve application performance through parallelism.

**Difference between Process and Thread**

1. Process is heavy weight or resource intensive. Thread is light weight, taking lesser resources than a process.
2. Process switching needs interaction with operating system. Thread switching does not need to interact with operating system.
3. In multiple processing environments, each process executes the same code but has its own memory and file resources. All threads can share same set of open files, child processes.
4. If one process is blocked, then no other process can execute until the first process is unblocked. While one thread is blocked and waiting, a second thread in the same task can run.
5. Multiple processes without using threads use more resources. Multiple threaded processes use fewer resources.
6. In multiple processes each process operates independently of the others. One thread can read, write or change another thread's data.

Advantages of Thread

    Threads minimize the context switching time.
    Use of threads provides concurrency within a process.
    Efficient communication.
    It is more economical to create and context switch threads.
    Threads allow utilization of multiprocessor architectures to a greater scale and efficiency.

Types of Thread

Threads are implemented in following two ways −

    User Level Threads − User managed threads.

    Kernel Level Threads − Operating System managed threads acting on kernel, an operating system core.

User Level Threads

In this case, the thread management kernel is not aware of the existence of threads. The thread library contains code for creating and destroying threads, for passing message and data between threads, for scheduling thread execution and for saving and restoring thread contexts. The application starts with a single thread.

Kernel Level Threads

In this case, thread management is done by the Kernel. There is no thread management code in the application area. Kernel threads are supported directly by the operating system. Any application can be programmed to be multithreaded. All of the threads within an application are supported within a single process.

The Kernel maintains context information for the process as a whole and for individuals threads within the process. Scheduling by the Kernel is done on a thread basis. The Kernel performs thread creation, scheduling and management in Kernel space. Kernel threads are generally slower to create and manage than the user threads.


**3.  Process Scheduling ( All the Job Scheduling Algorithms )**

The process scheduling is the activity of the process manager that handles the removal of the running process from the CPU and the selection of another process on the basis of a particular strategy.

Process scheduling is an essential part of a Multiprogramming operating systems. Such operating systems allow more than one process to be loaded into the executable memory at a time and the loaded process shares the CPU using time multiplexing.

Process Scheduling Queues

The OS maintains all PCBs in Process Scheduling Queues. The OS maintains a separate queue for each of the process states and PCBs of all processes in the same execution state are placed in the same queue. When the state of a process is changed, its PCB is unlinked from its current queue and moved to its new state queue.

The Operating System maintains the following important process scheduling queues −

    Job queue − This queue keeps all the processes in the system.

    Ready queue − This queue keeps a set of all processes residing in main memory, ready and waiting to execute. A new process is always put in this queue.

    Device queues − The processes which are blocked due to unavailability of an I/O device constitute this queue.

**4.  Important Scheduling Algos ( SJF , SRTF , FCFS , LJF(Longest Job First) and Round Robin Scheduling)**

A Process Scheduler schedules different processes to be assigned to the CPU based on particular scheduling algorithms. There are six popular process scheduling algorithms which we are going to discuss in this chapter −

    First-Come, First-Served (FCFS) Scheduling
    Shortest-Job-Next (SJN) Scheduling
    Priority Scheduling
    Shortest Remaining Time
    Round Robin(RR) Scheduling
    Multiple-Level Queues Scheduling

These algorithms are either non-preemptive or preemptive. Non-preemptive algorithms are designed so that once a process enters the running state, it cannot be preempted until it completes its allotted time, whereas the preemptive scheduling is based on priority where a scheduler may preempt a low priority running process anytime when a high priority process enters into a ready state.

First Come First Serve (FCFS)

    Jobs are executed on first come, first serve basis.
    It is a non-preemptive, pre-emptive scheduling algorithm.
    Easy to understand and implement.
    Its implementation is based on FIFO queue.
    Poor in performance as average wait time is high.

Shortest Job Next (SJN)

    This is also known as shortest job first, or SJF

    This is a non-preemptive, pre-emptive scheduling algorithm.

    Best approach to minimize waiting time.

    Easy to implement in Batch systems where required CPU time is known in advance.

    Impossible to implement in interactive systems where required CPU time is not known.

    The processer should know in advance how much time process will take.

Priority Based Scheduling

    Priority scheduling is a non-preemptive algorithm and one of the most common scheduling algorithms in batch systems.

    Each process is assigned a priority. Process with highest priority is to be executed first and so on.

    Processes with same priority are executed on first come first served basis.

    Priority can be decided based on memory requirements, time requirements or any other resource requirement.


Shortest Remaining Time

    Shortest remaining time (SRT) is the preemptive version of the SJN algorithm.

    The processor is allocated to the job closest to completion but it can be preempted by a newer ready job with shorter time to completion.

    Impossible to implement in interactive systems where required CPU time is not known.

    It is often used in batch environments where short jobs need to give preference.

Round Robin Scheduling

    Round Robin is the preemptive process scheduling algorithm.

    Each process is provided a fix time to execute, it is called a quantum.

    Once a process is executed for a given time period, it is preempted and other process executes for a given time period.

    Context switching is used to save states of preempted processes.

Multiple-Level Queues Scheduling

Multiple-level queues are not an independent scheduling algorithm. They make use of other existing algorithms to group and schedule jobs with common characteristics.

    Multiple queues are maintained for processes with common characteristics.
    Each queue can have its own scheduling algorithms.
    Priorities are assigned to each queue.


**5.  Process Synchronization , Critical Section , Inter Process Communication , Locks for Synchronization (Semaphore and Mutex) and Monitors (Important)**

**Process Synchronization**

On the basis of synchronization, processes are categorized as one of the following two types:

    Independent Process : Execution of one process does not affects the execution of other processes.
    Cooperative Process : Execution of one process affects the execution of other processes.

Process synchronization problem arises in the case of Cooperative process also because resources are shared in Cooperative processes.

**Critical Section Problem**

Critical section is a code segment that can be accessed by only one process at a time. Critical section contains shared variables which need to be synchronized to maintain consistency of data variables.

In the entry section, the process requests for entry in the Critical Section.


Any solution to the critical section problem must satisfy three requirements:


    Mutual Exclusion : If a process is executing in its critical section, then no other process is allowed to execute in the critical section.
    Progress : If no process is executing in the critical section and other processes are waiting outside the critical section, then only those processes that are not executing in their remainder section can participate in deciding which will enter in the critical section next, and the selection can not be postponed indefinitely.
    Bounded Waiting : A bound must exist on the number of times that other processes are allowed to enter their critical sections after a process has made a request to enter its critical section and before that request is granted.

Mutex and Semaphore both provide synchronization services but they are not the same. Details about both Mutex and Semaphore are given below −

**Mutex**

Mutex is a mutual exclusion object that synchronizes access to a resource. It is created with a unique name at the start of a program. The Mutex is a locking mechanism that makes sure only one thread can acquire the Mutex at a time and enter the critical section. This thread only releases the Mutex when it exits the critical section.

This is shown with the help of the following example −

```
wait (mutex);
…..
Critical Section
…..
signal (mutex);
```

A Mutex is different than a semaphore as it is a locking mechanism while a semaphore is a signalling mechanism. A binary semaphore can be used as a Mutex but a Mutex can never be used as a semaphore.
Semaphore

**Semaphore**

A semaphore is a signalling mechanism and a thread that is waiting on a semaphore can be signaled by another thread. This is different than a mutex as the mutex can be signaled only by the thread that called the wait function.

A semaphore uses two atomic operations, wait and signal for process synchronization.

The wait operation decrements the value of its argument S, if it is positive. If S is negative or zero, then no operation is performed.

```
wait(S)
{
   while (S<=0);
   S--;
}
```

The signal operation increments the value of its argument S.

```
signal(S)
{
   S++;
}
```

There are mainly two types of semaphores i.e. counting semaphores and binary semaphores.

* Counting Semaphores are integer value semaphores and have an unrestricted value domain. These semaphores are used to coordinate the resource access, where the semaphore count is the number of available resources.

* The binary semaphores are like counting semaphores but their value is restricted to 0 and 1. The wait operation only works when the semaphore is 1 and the signal operation succeeds when semaphore is 0.

**6.  DeadLock , Characteristics of DeadLock , Handling and Recovery from Deadlock**

**Deadlock in Operating System**

A process in operating systems uses different resources and uses resources in following way.

1) Requests a resource
2) Use the resource
2) Releases the resource



Deadlock is a situation where a set of processes are blocked because each process is holding a resource and waiting for another resource acquired by some other process.

**Deadlock can arise if following four conditions hold simultaneously (Necessary Conditions)**

Mutual Exclusion: One or more than one resource are non-sharable (Only one process can use at a time)

Hold and Wait: A process is holding at least one resource and waiting for resources.

No Preemption: A resource cannot be taken from a process unless the process releases the resource.

Circular Wait: A set of processes are waiting for each other in circular form.



**Methods for handling deadlock**

1) Deadlock prevention or avoidance: The idea is to not let the system into deadlock state.
One can zoom into each category individually, Prevention is done by negating one of above mentioned necessary conditions for deadlock. Avoidance is kind of futuristic in nature. By using strategy of “Avoidance”, we have to make an assumption. We need to ensure that all information about resources which process WILL need are known to us prior to execution of the process. We use Banker’s algorithm (Which is in-turn a gift from Dijkstra) in order to avoid deadlock.


2) Deadlock detection and recovery: Let deadlock occur, then do preemption to handle it once occurred.

3) Ignore the problem all together: If deadlock is very rare, then let it happen and reboot the system. This is the approach that both Windows and UNIX take.

The banker’s algorithm is a resource allocation and deadlock avoidance algorithm that tests for safety by simulating the allocation for predetermined maximum possible amounts of all resources, then makes an “s-state” check to test for possible activities, before deciding whether allocation should be allowed to continue.

Banker’s algorithm is named so because it is used in banking system to check whether loan can be sanctioned to a person or not. Suppose there are n number of account holders in a bank and the total sum of their money is S. If a person applies for a loan then the bank first subtracts the loan amount from the total money that bank has and if the remaining amount is greater than S then only the loan is sanctioned. It is done because if all the account holders comes to withdraw their money then the bank can easily do it.

In other words, the bank would never allocate its money in such a way that it can no longer satisfy the needs of all its customers. The bank would try to be in safe state always.

**7.  Memory Management in Operating System**

Memory management is the functionality of an operating system which handles or manages primary memory and moves processes back and forth between main memory and disk during execution. Memory management keeps track of each and every memory location, regardless of either it is allocated to some process or it is free. It checks how much memory is to be allocated to processes. It decides which process will get memory at what time. It tracks whenever some memory gets freed or unallocated and correspondingly it updates the status.

**8.  First Fit , Best Fit, Next Fit and Worst Fit in Operating System (Important)**

**Fragmentation**

As processes are loaded and removed from memory, the free memory space is broken into little pieces. It happens after sometimes that processes cannot be allocated to memory blocks considering their small size and memory blocks remains unused. This problem is known as Fragmentation.

Fragmentation is of two types −

External fragmentation

Total memory space is enough to satisfy a request or to reside a process in it, but it is not contiguous, so it cannot be used.

Internal fragmentation

Memory block assigned to process is bigger. Some portion of memory is left unused, as it cannot be used by another process.

* External fragmentation can be reduced by compaction or shuffle memory contents to place all free memory together in one large block. To make compaction feasible, relocation should be dynamic.

* The internal fragmentation can be reduced by effectively assigning the smallest partition but large enough for the process.

**First Fit**

In the first fit approach is to allocate the first free partition or hole large enough which can accommodate the process. It finishes after finding the first suitable free partition.

Advantage

Fastest algorithm because it searches as little as possible.

Disadvantage

The remaining unused memory areas left after allocation become waste if it is too smaller. Thus request for larger memory requirement cannot be accomplished.

**Best Fit**

The best fit deals with allocating the smallest free partition which meets the requirement of the requesting process. This algorithm first searches the entire list of free partitions and considers the smallest hole that is adequate. It then tries to find a hole which is close to actual process size needed.

Advantage

Memory utilization is much better than first fit as it searches the smallest free partition first available.

Disadvantage

It is slower and may even tend to fill up memory with tiny useless holes.

**Worst fit**

In worst fit approach is to locate largest available free portion so that the portion left will be big enough to be useful. It is the reverse of best fit.

Advantage

Reduces the rate of production of small gaps.

Disadvantage

If a process requiring larger memory arrives at a later stage then it cannot be accommodated as the largest hole is already split and occupied.

**9.  Paging in Memory Management (Concept of Virtual memory) (Important)**

**Paging**

A computer can address more memory than the amount physically installed on the system. This extra memory is actually called virtual memory and it is a section of a hard that's set up to emulate the computer's RAM. Paging technique plays an important role in implementing virtual memory.

Paging is a memory management technique in which process address space is broken into blocks of the same size called pages (size is power of 2, between 512 bytes and 8192 bytes). The size of the process is measured in the number of pages.

Similarly, main memory is divided into small fixed-sized blocks of (physical) memory called frames and the size of a frame is kept the same as that of a page to have optimum utilization of the main memory and to avoid external fragmentation.
Paging

Page address is called logical address and represented by page number and the offset.

```
Logical Address = Page number + page offset
```

Frame address is called physical address and represented by a frame number and the offset.

```
Physical Address = Frame number + page offset
```
A data structure called page map table is used to keep track of the relation between a page of a process to a frame in physical memory.

When the system allocates a frame to any page, it translates this logical address into a physical address and create entry into the page table to be used throughout execution of the program.

When a process is to be executed, its corresponding pages are loaded into any available memory frames. Suppose you have a program of 8Kb but your memory can accommodate only 5Kb at a given point in time, then the paging concept will come into picture. When a computer runs out of RAM, the operating system (OS) will move idle or unwanted pages of memory to secondary memory to free up RAM for other processes and brings them back when needed by the program.

This process continues during the whole execution of the program where the OS keeps removing idle pages from the main memory and write them onto the secondary memory and bring them back when required by the program.
Advantages and Disadvantages of Paging

Here is a list of advantages and disadvantages of paging −

    Paging reduces external fragmentation, but still suffer from internal fragmentation.

    Paging is simple to implement and assumed as an efficient memory management technique.

    Due to equal size of the pages and frames, swapping becomes very easy.

    Page table requires extra memory space, so may not be good for a system having small RAM.


**10. Demand Paging , Thrashing and Page Replacement Algo (FCFS and LRU Algorithm)**

**Virtual Memory**

extra memory is actually called virtual memory and it is a section of a hard disk that's set up to emulate the computer's RAM.

The main visible advantage of this scheme is that programs can be larger than physical memory. Virtual memory serves two purposes. First, it allows us to extend the use of physical memory by using disk. Second, it allows us to have memory protection, because each virtual address is translated to a physical address.

Following are the situations, when entire program is not required to be loaded fully in main memory.

    User written error handling routines are used only when an error occurred in the data or computation.

    Certain options and features of a program may be used rarely.

    Many tables are assigned a fixed amount of address space even though only a small amount of the table is actually used.

    The ability to execute a program that is only partially in memory would counter many benefits.

    Less number of I/O would be needed to load or swap each user program into memory.

    A program would no longer be constrained by the amount of physical memory that is available.

    Each user program could take less physical memory, more programs could be run the same time, with a corresponding increase in CPU utilization and throughput.

**Demand Paging**

A demand paging system is quite similar to a paging system with swapping where processes reside in secondary memory and pages are loaded only on demand, not in advance. When a context switch occurs, the operating system does not copy any of the old program’s pages out to the disk or any of the new program’s pages into the main memory Instead, it just begins executing the new program after loading the first page and fetches that program’s pages as they are referenced.
Demand Paging

While executing a program, if the program references a page which is not available in the main memory because it was swapped out a little ago, the processor treats this invalid memory reference as a page fault and transfers control from the program to the operating system to demand the page back into the memory.
Advantages

Following are the advantages of Demand Paging −

    Large virtual memory.
    More efficient use of memory.
    There is no limit on degree of multiprogramming.

Disadvantages

    Number of tables and the amount of processor overhead for handling page interrupts are greater than in the case of the simple paged management techniques.

**Thrashing**

To know what is thrashing, you must first be aware of swapping and page fault. So lets start with those concepts:

First we need to know what actually happens inside your OS that makes your system behave as if it has a very large memory. In operating systems that implement a virtual memory space, the programs  allocate memory from an address space that may be much larger than the  actual amount of RAM the system possesses. OS decides which program's memory is actually in RAM at any specific instant of time.

Page Fault and Swapping: A page fault occurs when the memory access requested (from the virtual  address space) does not map to something that is in RAM. A page must  then be sent from RAM to swap, so that the requested new page can be  brought from swap to RAM. This results in 2 disk I/Os. Now you might know that disk I/Os are very slow as compared to memory access.

Thrashing: Now if it happens that your system has to swap pages at such a higher rate that major chunk of CPU time is spent in swapping then this state is known as thrashing. So effectively during thrashing, the CPU spends less time in some actual productive work and more time in swapping.

Now the effects of thrashing and also the extent to which thrashing occurs will be decided by the type of page replacement policy.

1. Global Page Replacement: The paging algorithm is applied to  all the pages of the memory regardless of which process "owns" them. A  page fault in one process may cause a replacement from any process in  memory. Thus, the size of a partition may vary randomly.

2. Local Page Replacement: The memory is divided into partitions of a predetermined size for each  process and the paging algorithm is applied independently for each  region. A process can only use pages in its partition.

**What happens after Thrashing starts?**

If global page replacement is used, situations worsens very quickly. CPU thinks that CPU utilization is decreasing, so it tries to increase the degree of multiprogramming. Hence bringing more processes inside memory, which in effect increases the thrashing and brings down CPU utilization further down. The CPU notices that utilization is going further down, so it increases the degree of multiprogramming further and the cycle continues.

The solution can be local page replacement where a process can only be allocated pages in its own region in memory. If the swaps of a process increase also, the overall CPU utilization does not decrease much. If other transactions have enough page frames in the partitions they occupy, they will continue to be processed efficiently. 

But local page replacement has its own disadvantages which you can now explore further.

**Page Replacement Algorithms**

Page replacement algorithms are the techniques using which an Operating System decides which memory pages to swap out, write to disk when a page of memory needs to be allocated. Paging happens whenever a page fault occurs and a free page cannot be used for allocation purpose accounting to reason that pages are not available or the number of free pages is lower than required pages.

When the page that was selected for replacement and was paged out, is referenced again, it has to read in from disk, and this requires for I/O completion. This process determines the quality of the page replacement algorithm: the lesser the time waiting for page-ins, the better is the algorithm.

A page replacement algorithm looks at the limited information about accessing the pages provided by hardware, and tries to select which pages should be replaced to minimize the total number of page misses, while balancing it with the costs of primary storage and processor time of the algorithm itself. There are many different page replacement algorithms. We evaluate an algorithm by running it on a particular string of memory reference and computing the number of page faults,

**FCFS**

    Oldest page in main memory is the one which will be selected for replacement.

    Easy to implement, keep a list, replace pages from the tail and add new pages at the head.

**Optimal page Replacement Algo**

    An optimal page-replacement algorithm has the lowest page-fault rate of all algorithms. An optimal page-replacement algorithm exists, and has been called OPT or MIN.

    Replace the page that will not be used for the longest period of time. Use the time when a page is to be used.

**LRU**

    Page which has not been used for the longest time in main memory is the one which will be selected for replacement.

    Easy to implement, keep a list, replace pages by looking back into time.

**11. Segmentation in Memory Management and Translation Lookaside Buffer (TLB)**

**Segmentation**

Segmentation is a memory management technique in which each job is divided into several segments of different sizes, one for each module that contains pieces that perform related functions. Each segment is actually a different logical address space of the program.

When a process is to be executed, its corresponding segmentation are loaded into non-contiguous memory though every segment is loaded into a contiguous block of available memory.

Segmentation memory management works very similar to paging but here segments are of variable-length where as in paging pages are of fixed size.

A program segment contains the program's main function, utility functions, data structures, and so on. The operating system maintains a segment map table for every process and a list of free memory blocks along with segment numbers, their size and corresponding memory locations in main memory. For each segment, the table stores the starting address of the segment and the length of the segment. A reference to a memory location includes a value that identifies a segment and an offset.

**Translation Lookaisde Buffer**

In Operating System (Memory Management Technique : Paging), for each process page table will be created, which will contain Page Table Entry (PTE). This PTE will contain information like frame number (The address of main memory where we want to refer), and some other useful bits (e.g., valid/invalid bit, dirty bit, protection bit etc). This page table entry (PTE) will tell where in the main memory the actual page is residing.

Now the question is where to place the page table, such that overall access time (or reference time) will be less.

The problem initially was to fast access the main memory content based on address generated by CPU (i.e logical/virtual address). Initially, some people thought of using registers to store page table, as they are high-speed memory so access time will be less.

The idea used here is, place the page table entries in registers, for each request generated from CPU (virtual address), it will be matched to the appropriate page number of the page table, which will now tell where in the main memory that corresponding page resides. Everything seems right here, but the problem is register size is small (in practical, it can accommodate maximum of 0.5k to 1k page table entries) and process size may be big hence the required page table will also be big (lets say this page table contains 1M entries), so registers may not hold all the PTE’s of Page table. So this is not a practical approach.

To overcome this size issue, the entire page table was kept in main memory. but the problem here is two main memory references are required:

    To find the frame number
    To go to the address specified by frame number

To overcome this problem a high-speed cache is set up for page table entries called a Translation Lookaside Buffer (TLB). Translation Lookaside Buffer (TLB) is nothing but a special cache used to keep track of recently used transactions. TLB contains page table entries that have been most recently used. Given a virtual address, the processor examines the TLB if a page table entry is present (TLB hit), the frame number is retrieved and the real address is formed. If a page table entry is not found in the TLB (TLB miss), the page number is used to index the process page table. TLB first checks if the page is already in main memory, if not in main memory a page fault is issued then the TLB is updated to include the new page entry.