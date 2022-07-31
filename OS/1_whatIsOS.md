# OS:

* A software that manages software and hardware components
* Act as a bridge between computer programs and hardware devices
* Example: Windows 10, Mac OS X, Debian, Fedora, Android

## Kernel:

* Makes hardware and software interact with each other

* Brain of linux os

* Act as bridge between hardware and software

* Component of Operating System

* First thing to load on startup

* It is a core of the os

* Responsible for:
    -allocating tasks for cpu
    -allocating memory to running programs
    -allocating requests from/to applications for input/output
    -inter-process communication(betwen the processes)

 * runs in protected area of memory(kernel space) whereas user actions are in another part of memory(user space)

Two types of kernel :(Windows & mac uses both)

   1. Monolithic kernel
       
        * runs all the operating system instructions in same address base (for speed) 

        * linux uses it

   2. Micro kernel

       * uses user space for modularity

       * herd uses it (apdina🤷‍♂)

(Old linux kernel available at kernel.org)

Refer: https://www.youtube.com/watch?v=rc27jtfyEpU&t=611

https://developer.ibm.com/articles/l-linux-kernel/
