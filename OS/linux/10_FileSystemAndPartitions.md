## File System in Linux

- A partition is a logical part of the disk.

- A filesystem is a method of storing/finding files on a hard disk.

- By dividing the hard disk into partitions, data can be grouped and separated as needed. When a failure or mistake occurs, only the data in the affected partition will be damaged, while the data on the other partitions will likely survive.

- The boot process has multiple steps, starting with BIOS, which triggers the boot loader to start up the Linux kernel. From there, the initramfs filesystem is invoked, which triggers the init program to complete the startup process.

- Determining the appropriate distribution to deploy requires that you match your specific system needs to the capabilities of the different distributions.

## Filesystem in Detail

1. Ext, Ext2, Ext3 and Ext4 file system

  - The file system Ext stands for Extended File System. It was primarily developed for MINIX OS. The Ext file system is an older version, and is no longer used due to some limitations.

  - Ext2 is the first Linux file system that allows managing two terabytes of data.

  - Ext3 is developed through Ext2; it is an upgraded version of Ext2 and contains backward compatibility. 

  - Ext4 file system is the faster file system among all the Ext file systems. It is a very compatible option for the SSD (solid-state drive) disks, and it is the default file system in Linux distribution.

2. JFS File System

  - JFS stands for Journaled File System, and it is developed by IBM for AIX Unix. It is an alternative to the Ext file system.

3. ReiserFS File System

  - ReiserFS is an alternative to the Ext3 file system. It has improved performance and advanced features.

4. Btrfs File System

  - Btrfs stands for the B tree file system. It is used for fault tolerance, repair system, fun administration, extensive storage configuration, and more.

5. Swap File System

  - The swap file system is used for memory paging in Linux operating system during the system hibernation.
