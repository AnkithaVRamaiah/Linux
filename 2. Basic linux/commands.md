

Here’s a detailed breakdown of basic Linux commands categorized by their functions. Each section covers commonly used commands with explanations and examples to help you understand how they work.

### 1. **Navigation**
Navigation commands help you explore the file system in Linux.

| Command          | Description                                                                 | Example                                                                                          |
|------------------|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| `pwd`            | Prints the current working directory (path).                                | `pwd`                                                                                             |
| `ls`             | Lists files and directories in the current directory.                      | `ls`                                                                                              |
| `cd`             | Changes the current directory.                                               | `cd /home/user/Documents` (Change to a directory)                                                |
| `cd ~`           | Navigates to the home directory.                                             | `cd ~` (Takes you to the home directory)                                                         |
| `cd ..`          | Moves one directory up (parent directory).                                  | `cd ..` (Move up one directory level)                                                            |
| `ls -l`          | Lists files in long format, showing detailed information (permissions, size, etc.). | `ls -l`                                                                                           |
| `ls -a`          | Lists all files including hidden files.                                     | `ls -a`                                                                                           |
| `ls -R`          | Lists files and directories recursively.                                    | `ls -R`                                                                                           |
| `find`             | Searches for files and directories in a directory hierarchy.               | `find /home/user -name "*.txt"` (Finds all `.txt` files in `/home/user` and its subdirectories)    |
| `locate`           | Quickly finds files and directories (based on an updated database).        | `locate file.txt` (Finds `file.txt` using the prebuilt index of files)                            |
| `which`            | Displays the full path of a command or executable.                          | `which python` (Shows the path of the `python` executable)                                        |
| `whereis`          | Locates binary, source, and man page files for a command.                  | `whereis ls` (Finds the binary, source, and man page for `ls`)                                    |

### 2. **File Operations**
File operations commands are used to manipulate files and directories.

| Command             | Description                                                                  | Example                                                                                           |
|---------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| `touch`             | Creates an empty file if it doesn’t exist or updates the timestamp if it does. | `touch file.txt` (Creates a file named `file.txt` if it doesn’t exist)                           |
| `mkdir`             | Creates a new directory.                                                     | `mkdir new_directory`                                                                             |
| `rmdir`             | Removes an empty directory.                                                  | `rmdir old_directory`                                                                            |
| `rm`                | Removes files or directories.                                                | `rm file.txt` (Removes `file.txt`)                                                                |
| `rm -r`             | Removes directories and their contents recursively.                           | `rm -r directory_name` (Deletes a directory and its contents)                                     |
| `cp`                | Copies files or directories.                                                 | `cp source.txt destination.txt` (Copies `source.txt` to `destination.txt`)                       |
| `cp -r`             | Copies directories recursively.                                              | `cp -r dir1 dir2` (Copies the entire directory `dir1` to `dir2`)                                  |
| `mv`                | Moves or renames files and directories.                                      | `mv old.txt new.txt` (Renames `old.txt` to `new.txt`)                                            |
| `mv -r`             | Moves directories recursively.                                               | `mv dir1 dir2` (Moves `dir1` to `dir2`)                                                          |
| `ln`                | Creates a hard link to a file.                                               | `ln file.txt file_link` (Creates a hard link named `file_link` pointing to `file.txt`)            |
| `ln -s`             | Creates a symbolic (soft) link to a file.                                    | `ln -s /path/to/original /path/to/link` (Creates a symlink from the original file to the link)     |
| `stat`             | Displays detailed information about a file or directory.                  | `stat file.txt` (Shows file size, permissions, last access time, etc.)                            |
| `split`            | Splits a file into smaller parts.                                          | `split -l 1000 largefile.txt` (Splits `largefile.txt` into smaller files with 1000 lines each)     |
| `cat > file.txt`   | Creates or overwrites a file using the `cat` command.                      | `cat > newfile.txt` (Start typing content for the file, press Ctrl+D to save and exit)            |
| `tee`              | Reads from standard input and writes to both standard output and files.    | `echo "Hello" | tee file.txt` (Writes "Hello" to both terminal and `file.txt`)                     |
| `tar`              | Archives multiple files into a single compressed file.                    | `tar -cvf archive.tar /path/to/files` (Creates a tar archive from specified files)                |
| `zip`              | Compresses files into a `.zip` archive.                                    | `zip archive.zip file1.txt file2.txt` (Zips multiple files into one archive)                     |
| `unzip`            | Extracts files from a `.zip` archive.                                      | `unzip archive.zip` (Extracts all files from the archive)                                         |
| `gzip`             | Compresses files using the gzip format.                                    | `gzip file.txt` (Compresses `file.txt` into `file.txt.gz`)                                        |
| `gunzip`           | Decompresses `.gz` files.                                                  | `gunzip file.txt.gz` (Decompresses `file.txt.gz` back to `file.txt`)                              |

### 3. **File Viewing**
These commands are used to view the contents of files.

| Command             | Description                                                                  | Example                                                                                           |
|---------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| `cat`               | Displays the contents of a file.                                             | `cat file.txt`                                                                                   |
| `tac`               | Displays the contents of a file in reverse (from bottom to top).              | `tac file.txt`                                                                                   |
| `more`              | Displays file content one page at a time (useful for large files).           | `more largefile.txt`                                                                              |
| `less`              | Similar to `more`, but allows for backward navigation through the file.      | `less file.txt`                                                                                  |
| `head`              | Displays the first few lines of a file (default is 10).                      | `head file.txt`                                                                                  |
| `tail`              | Displays the last few lines of a file (default is 10).                       | `tail file.txt`                                                                                  |
| `head -n 20`        | Displays the first 20 lines of a file.                                        | `head -n 20 file.txt`                                                                             |
| `tail -n 20`        | Displays the last 20 lines of a file.                                         | `tail -n 20 file.txt`                                                                             |
| `tail -f`           | Continuously watches a file for changes (useful for logs).                   | `tail -f /var/log/syslog` (Displays updates to the syslog)                                        |
| `vi`               | A powerful text editor used to view and edit files.                        | `vi file.txt` (Opens `file.txt` in the `vi` editor)                                               |
| `nano`             | A simple terminal text editor.                                             | `nano file.txt` (Opens `file.txt` in the `nano` editor)                                           |
| `file`             | Determines the type of a file (e.g., text, binary, executable).            | `file file.txt` (Shows the type of `file.txt`)                                                     |
| `wc`               | Counts words, lines, and characters in a file.                             | `wc file.txt` (Counts lines, words, and characters in `file.txt`)                                 |
| `shasum`           | Computes SHA-1 checksums for files.                                         | `shasum file.txt` (Displays the SHA-1 checksum of `file.txt`)                                      |
| `md5sum`           | Computes MD5 checksums for files.                                          | `md5sum file.txt` (Displays the MD5 checksum of `file.txt`)                                        |
| `hexdump`          | Dumps the content of a file in hexadecimal format.                         | `hexdump -C file.txt` (Shows hexadecimal and ASCII representations of `file.txt`)                 |

### 4. **Permissions**
File permissions commands are used to manage file access.

| Command             | Description                                                                  | Example                                                                                           |
|---------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| `chmod`             | Changes the permissions of a file or directory.                              | `chmod 755 file.txt` (Grants read, write, and execute permissions to the owner and read & execute permissions to others) |
| `chmod +x`          | Adds execute permission to a file.                                           | `chmod +x script.sh` (Makes `script.sh` executable)                                               |
| `chmod -x`          | Removes execute permission from a file.                                      | `chmod -x script.sh` (Makes `script.sh` non-executable)                                           |
| `chown`             | Changes the ownership of a file or directory.                                | `chown user:group file.txt` (Changes the owner and group of `file.txt`)                           |
| `chown -R`          | Recursively changes ownership of files and directories.                      | `chown -R user:group /dir` (Changes ownership of all files inside `/dir`)                         |
| `chgrp`             | Changes the group ownership of a file or directory.                          | `chgrp group file.txt` (Changes the group ownership of `file.txt` to `group`)                    |
| `umask`             | Sets the default file creation permissions (mask).                           | `umask 022` (Sets the default permissions to `755` for new files)                                |
| `setfacl`          | Sets file access control lists (ACLs) for files, allowing for more granular permission settings. | `setfacl -m u:username:rwx file.txt` (Grants `username` read, write, and execute permissions on `file.txt`) |
| `getfacl`          | Retrieves the current ACLs of a file.                                      | `getfacl file.txt` (Displays the ACL for `file.txt`)                                               |
| `umask`            | Sets the default file creation permissions for new files.                 | `umask 027` (Sets the default permission mask to `rw-r-----`)                                     |
| `sudo`             | Executes commands with elevated privileges (admin access).                | `sudo chmod 777 file.txt` (Changes file permissions with administrative privileges)                |

### 5. **System Information**
System information commands provide details about the system’s hardware and software.

| Command             | Description                                                                  | Example                                                                                           |
|---------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| `uname`             | Displays information about the system.                                        | `uname -a` (Shows all system information, including kernel version and architecture)             |
| `hostname`          | Displays or sets the system's hostname.                                       | `hostname` (Displays the current hostname)                                                        |
| `uptime`            | Displays how long the system has been running.                                | `uptime`                                                                                          |
| `top`               | Displays real-time information about system processes and resource usage.    | `top`                                                                                             |
| `htop`              | An interactive version of `top` with more features.                           | `htop` (Requires installation: `sudo apt install htop`)                                           |
| `free`              | Displays information about memory usage.                                      | `free -h` (Shows memory usage in human-readable format)                                           |
| `df`                | Displays information about disk space usage.                                  | `df -h` (Shows disk usage in a human-readable format)                                             |
| `du`                | Displays disk usage of files and directories.                                 | `du -sh /path/to/dir` (Shows the total disk usage of a directory)                                 |
| `ps`                | Displays information about running processes.                                | `ps aux` (Shows all running processes)                                                           |
| `ps -ef`            | Displays a more detailed view of all running processes.                       | `ps -ef`                                                                                          |
| `kill`              | Terminates a running process by its PID (Process ID).                         | `kill 1234` (Kills the process with PID `1234`)                                                   |
| `killall`           | Terminates processes by name.                                                 | `killall firefox` (Kills all processes named `firefox`)                                           |
| `lscpu`             | Displays information about the CPU architecture.                             | `lscpu`                                                                                           |
| `lspci`             | Displays information about PCI buses and devices.                            | `lspci`                                                                                           |
| `lsusb`             | Displays information about USB devices.                                       | `lsusb`                                                                                           |
| `dmesg`             | Displays kernel-related messages, useful for troubleshooting hardware issues. | `dmesg | tail` (Shows the last few kernel messages)                                               |
| `dstat`            | Displays various system resource statistics (CPU, memory, disk, etc.).     | `dstat` (Displays live stats on CPU, disk, and memory usage)                                       |
| `vmstat`           | Displays system virtual memory statistics.                                 | `vmstat` (Shows memory, process, and system statistics)                                            |
| `iostat`           | Displays input/output statistics for devices and partitions.               | `iostat` (Shows CPU and I/O statistics for devices)                                                |
| `netstat`          | Displays network connections, routing tables, interface statistics, etc.   | `netstat -tuln` (Shows all listening ports and associated addresses)                               |
| `ss`               | Utility to investigate sockets (network connections).                      | `ss -tuln` (Shows all active listening ports and their details)                                    |
| `uptime`           | Shows system uptime along with load averages.                              | `uptime` (Displays how long the system has been running and the system load)                       |
| `lshw`             | Displays detailed hardware configuration of the system.                    | `sudo lshw -short` (Lists hardware in a concise format)                                            |
| `lsblk`            | Lists information about all available block devices.                       | `lsblk` (Displays information about available block devices like hard drives)                      |
| `fdisk`            | Used to partition disks.                                                   | `sudo fdisk -l` (Lists all partitions on the system)                                              |
| `ps aux`           | Shows all running processes with details.                                  | `ps aux` (Shows all running processes with user, PID, and resource usage)                         |
| `uptime`           | Shows how long the system has been running and its load averages.          | `uptime`                                                                                          |
| `watch`            | Executes a command at regular intervals and updates the output.            | `watch df -h` (Runs `df -h` every 2 seconds, useful for monitoring disk usage in real-time)        |
| `lsmod`            | Displays the status of loaded modules.                                     | `lsmod` (Lists currently loaded kernel modules)                                                   |

### Additional Commands

| Command             | Description                                                                  | Example                                                                                           |
|---------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| `man`               | Displays the manual (help) for a command.                                     | `man ls` (Shows the manual for the `ls` command)                                                  |
| `alias`             | Creates an alias for a command.                                               | `alias ll='ls -l'` (Creates an alias for `ls -l` as `ll`)                                          |
| `history`           | Displays the command history.                                                 | `history`                                                                                         |
| `clear`             | Clears the terminal screen.                                                  | `clear`                                                                                           |



### 6. **Process Management (Additional Commands)**
Commands to manage system processes more effectively.

| Command            | Description                                                                | Example                                                                                           |
|--------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| `bg`               | Resumes a suspended job in the background.                                 | `bg %1` (Resumes job number 1 in the background)                                                  |
| `fg`               | Brings a background job to the foreground.                                | `fg %1` (Brings job number 1 to the foreground)                                                  |
| `jobs`             | Lists all active jobs in the current session.                             | `jobs`                                                                                             |
| `nohup`            | Runs a command immune to hangups, used for long-running processes.         | `nohup command &` (Runs `command` in the background, even after logging out)                       |
| `pkill`            | Kills processes by name.                                                  | `pkill firefox` (Kills all processes named `firefox`)                                              |
| `pstree`           | Displays running processes in a tree-like format.                         | `pstree` (Displays a process tree of running processes)                                            |

