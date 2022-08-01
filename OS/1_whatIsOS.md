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

- Two types of kernel :(Windows & mac uses both)

   1. Monolithic kernel
       
        * Runs all the operating system instructions in same address base (for speed) 

        * Linux uses it

   2. Micro kernel

       * Uses user space for modularity

       * Herd uses it (apdina🤷‍♂.. i think many ppl uses it adha dhan apdi solluraga pola 😅)

- (Old linux kernel available at kernel.org)

- Refer: https://www.youtube.com/watch?v=rc27jtfyEpU&t=611 and https://developer.ibm.com/articles/l-linux-kernel/


## Processes:

* An instance of program which loaded into memory is called process

* It contains code for program and and the process state

* Example(from SEC201)

   - A program is a series of instructions. Like a shopping list, the list itself doesn’t do anything on its own 
   - A person reads the shopping list, and then purchases the items on the list. 
   - Halfway through the list, they have already bought some items and still need to buy some more. This is the ‘state’ of the process.

## Interrupt:

* A signal sent to hardware or software to indicate an event needs immediate action

* Then processor suspends it current activities, saving it state , and calls interrupt handler to handle the event

* Once the event caused the interrupt is handled, the processor state is restored

* Example (from SEC201)
   - Typing on a keyboard. 
   - The keypress sends an interrupt signal, causing the processor to read the keystroke.

## Boot Loader: 

* A program that boots the operating system

* A small computer program on motherboard

* Runs when the computer is booting up

* Then it will perform hardware diagnostics before loading operating system

* Mordern computers uses uefi boot loader, old computer uses bios (these things depends on age of motherboard)

* It can control things like which disk to check for os (useful during dual boot), etc

* Example: GRUB, ISOLINUX
