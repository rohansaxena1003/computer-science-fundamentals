What is a program and a process ?
    A program is a piece of code( or instructions ) that is lying 
    idle in our device/system.
    When this program is run, it becomes a process.

What are mechanisms and policies ?
    To create an illusion that system has infinite number of CPUs,
    the OS uses low-level machinery known as 'mechanisms'. These 
    mechanisms are used to determine time sharing 
    The high level machinery is called 'policies'.
    So, mechanisms decide how to run a program and policies determine which program should the OS run. 

What is 'machine state' of a process ?
    Every component of a machine affected during a process constitutes its machine 
    state. 
    1st component is the memory of the machine because the instructions 
    and data related to the process are stored in it. Also the part of the memory 
    that a process can access is called its 'address space'.'
    2nd component is 'registers'. Many instructions need to access(read or update) registers. Program Counter(PC) and Stack Pointer are two important registers.
    3rd component is persistent storage devices.

Process related API
    1. Create: An API to create new processes. Eg. When you click on an application icon, the OS creates a new process to run a program.
    2. Destroy: Same as above, this method forcefully destroys a process.
    3. Wait: This waits for a process to finish and then this API is invoked.
    4. Status: This API tells the status of the process, i.e, current state of the
    process, its duration etc.
    5. Misc control: These are different from above like suspend or resume a process.

How does OS create a process ?
    A program is stored in disk space(SSD in today's time). So the first step for
    the OS is to read the bytes in the disk and load the program and its data into 
    the address space. In earlier times, this loading used to be done 'eagerly' (load all the data at once before running the program). Now, this is done 'lazily' ( load data by bit as and when required ). This bit by bit work is done using 'Paging' and 'Swapping' techniques.
    The second step is to allocate some memory to run-time stack(also called stack).
    This stack stores local variables, function parameters and return addresses. The OS
    may also allocate some memory for 'heap'. This heap is explicitly used to store
    dynamically allocated data and is needed for DS like LL, hash tables, trees etc.
    Initially, the heap is small in size but it can grow very during the process. It 
    asks for more memory from the OS by using malloc() API.
    The third step is to some initialization tasks related to I/O.
    The last step is to start the program at main() and handover control of part of
    CPU to the process.

Different states of a process(3 basic states)
    1. Running: The process is running(executing instructions).
    2. Ready: The process is ready to run but the OS for some reason has avoided 
    running it.
    3. Blocked: The process is blocked from running until some event takes place. Eg. a 
    process is waiting for input from user.

