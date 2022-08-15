## Directory Structure

- Linux systems store their important files according to a standard layout called the Filesystem Hierarchy Standard (FHS)

- Linux uses the ‘/’ character to separate paths (unlike Windows, which uses ‘\’), and does not have drive letters

- Multiple drives and/or partitions are mounted as directories in the single filesystem. 

- Removable media such as USB drives and CDs and DVDs will show up as mounted at /run/media/yourusername/disklabel for recent Linux systems, or under /media for older distributions. 

- For example, if your username is student a USB pen drive labeled FEDORA might end up being found at /run/media/student/FEDORA, and a file README.txt on that disc would be at /run/media/student/FEDORA/README.txt.
