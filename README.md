📂 Customised Virtual File System (CVFS)
📌 Overview

Customised Virtual File System (CVFS) is a simulation of a Linux-like file system implemented in C.
This project demonstrates the internal working of file operations such as create, open, read, write, lseek, close, delete, etc., entirely in memory.

The system mimics core file system components like Superblock, Inode, File Table, and UFDT.

🚀 Features

Create file

Open file

Read file

Write file

Close file

Delete file

Truncate file

Change file offset (lseek)

Display file statistics (stat / fstat)

List files

🛠 Technologies Used

C Programming Language

Data Structures (Linked List, Arrays)

Pointers

Dynamic Memory Allocation

Operating System Concepts

🖥 Platform

Windows / Linux

GCC Compiler

🧠 Concepts Implemented

Superblock management

Inode structure

User File Descriptor Table (UFDT)

File Table

Reference Count & Link Count

File offset handling

Memory management

📊 Architecture

CVFS consists of:

Superblock – Maintains metadata of file system

DILB (Linked List of Inodes) – Stores file metadata

UFDT – Stores opened file descriptors

File Table – Maintains runtime file information

⚙ How To Run
Compile:
gcc cvfs.c -o cvfs
Run:
./cvfs
📖 Supported Commands
creat <filename> <permission>
open <filename> <mode>
read <filename> <bytes>
write <filename>
close <filename>
closeall
ls
stat <filename>
fstat <fd>
truncate <filename>
rm <filename>
lseek <filename> <offset> <startpoint>
exit

Permission/Mode:

1 → Read

2 → Write

3 → Read & Write

📌 Example
creat demo 3
write demo
read demo 10
stat demo
rm demo
🎯 Learning Outcome

This project helped in understanding:

Internal working of file systems

OS file management

System call simulation

Data structure implementation in real applications

🔮 Future Improvements

Add directory support

Add execute permission

Add multi-user support

Store data permanently instead of RAM

👨‍💻 Author

Akash Malgunde
