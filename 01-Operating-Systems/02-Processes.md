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