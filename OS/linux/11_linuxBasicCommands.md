## Linux commands:


### echo 
- print whatever input we gave to it
```
root@localhost:~# echo anytext
anytext
```

### whoami
- shows which user i was logged in
```
root@localhost:~# whoami
root
```

## Navigation

### ls (listing)
- list files in current directory
- (Pro tip: use ls -la whenever listing files yena adu dha hidden files and file ku irukura permissions a serthu kaatum)
```
root@localhost:~# ls
Desktop    Music     Templates
Documents  Pictures  Videos
Downloads  Public 
```

### cd (change directory)
 - Navigate to another directory
```
root@localhost:~# cd Desktop
root@localhost:~/Desktop#
```

### cat (concatenate)
 - Shows output of a file
```
root@localhost:~# cat a.txt
Lola
```

### pwd (print working directory)
 - Shows which directory we are in
```
root@localhost:~# pwd
/root
```


## Searching files

### find
 - Find the location of files
1. using name
```
~ $ find -name filename.txt
./Desktop/filename.txt
```
2. If we dont know the name? It'll list all files of similar type
```
~ $ find -name *.txt
```

#### Advanced:
Syntax: 
```
find [where] [what]
```
To search whole pc: 
```
find /
```

Flags:
```
-type : Search file or directory (d - directory, f - file)
-name : Search name or pattern(if we using wildcard[*], we need to give command in quotes or else wont work. -iname is same as -name but case insensitive)
-exec : can use it in your find command to execute a new command, following the -exec flag, like so: -exec whoami \; (this command is used mostly for priviledge escalation, will learn later :)
-user : owner of file
-size : file size (use -n, n, +n to find file size accordingly. Suffix is c for bytes, k for kb's , M for mb's [eg: +1000m for greater than 1000mb filesize] )
-perm : find using file permissions (eg: u=f or 777 method [will show which exactly matches this]. - will return atleast this permission [-444 will match files that are readable by everyone, even if someone also has write and/or execute permissions]. / will return files with any one of the number [eg: /666 mode will match files that are readable and writeable by at least one of the groups (owner, group, or others)] )
```

Time related(-min, -time):

Prefix:
```
-a : last accessed
-m : last modified
-c : last changed
```
(-amin +30 shows files last access time more than 30mins, -mtime -7 shows files modified less than 7 days ago[Note: when you want to specify that a file was modified within the last 24 hours, the option -mtime 0 is used])
*you can use the redirection operator > with the find command to save the result of search (use '2>/dev/null' to supress error output. This way, you won’t see any results you’re not allowed to access)
*

* grep
 - Used to search inside files (itll grab a line with the given condition and prints it)
```
~ $ grep 'THM' access.log
THM(access) == tryhackme
```

## Shell operators:

### & 
- used to run commands in background (will come handy when copying large files)

### &&
 - combine multiple commands in one line
```
~ $ cd Desktop && ls
```
command 2 will run only if command 1 is successful

### >
 - redirect one command output to elsewhere
```
~ $ cat a.txt
Lalalalalala
~ $ echo helloWorld > a.txt
~ $ cat a.txt
helloWorld
```
Note: it will override the previous content so be careful🥲

### >>
 - same as > but it will append content at end of the file instead of overwriting
```
~ $ cat a.txt
Lalalalalala
~ $ echo helloWorld > a.txt
~ $ cat a.txt
Lalalalalala
helloWorld
```
