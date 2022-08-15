## BIOS (booting process) : 

* BIOS will initalize hardware and tests main memory(RAM).

* Also known as POST(Power On Self Test).

* It is stored on ROM, when pc is turned on, it is loaded into main memory

* After this , boot process will be controlled by OS(boot loader)

## Boot Loader : 
 - (in general) Once the POST is completed, the system control passes from the BIOS to the boot loader. 
 - The boot loader is usually stored on one of the hard disks in the system, either in the boot sector (for traditional BIOS/MBR systems) or the EFI partition (for more recent (Unified) Extensible Firmware Interface or EFI/UEFI systems). 
 - Up to this stage, the machine does not access any mass storage media. Thereafter, information on date, time, and the most important peripherals are loaded from the CMOS (complementary metal oxide semiconductor) values (after a technology used for the battery-powered memory store which allows the system to keep track of the date and time even when it is powered off).
 
 - (in linux) A number of boot loaders exist for Linux; the most common ones are GRUB (for GRand Unified Boot loader), ISOLINUX (for booting from removable media), and DAS U-Boot (for booting on embedded devices/appliances). 
 - Most Linux boot loaders can present a user interface for choosing alternative options for booting Linux, and even other operating systems that might be installed. 
 - When booting Linux, the boot loader is responsible for loading the kernel image and the initial RAM disk or filesystem (which contains some critical files and device drivers needed to start the system) into memory.
 
## Master Boot Record (MBR)

- Short for master boot record, MBR is also sometimes referred to as the master boot block, master partition boot sector, and sector 0. 
- The MBR is the first sector of the computer hard drive. 
- It tells the computer how the hard drive is partitioned, and how to load the operating system.
- More at https://www.computerhope.com/jargon/m/mbr.htm

## Booting process

The boot loader has two distinct stages:

- For systems using the BIOS/MBR method, the boot loader resides at the first sector of the hard disk, also known as the Master Boot Record (MBR). The size of the MBR is just 512 bytes. In this stage, the boot loader examines the partition table and finds a bootable partition. Once it finds a bootable partition, it then searches for the second stage boot loader, for example GRUB, and loads it into RAM (Random Access Memory). For systems using the EFI/UEFI method, UEFI firmware reads its Boot Manager data to determine which UEFI application is to be launched and from where (i.e. from which disk and partition the EFI partition can be found). The firmware then launches the UEFI application, for example GRUB, as defined in the boot entry in the firmware's boot manager. This procedure is more complicated, but more versatile than the older MBR methods.

- The second stage boot loader resides under /boot. A splash screen is displayed, which allows us to choose which operating system (OS) to boot. After choosing the OS, the boot loader loads the kernel of the selected operating system into RAM and passes control to it.  Kernels are almost always compressed, so its first job is to uncompress itself. After this, it will check and analyze the system hardware and initialize any hardware device drivers built into the kernel.
