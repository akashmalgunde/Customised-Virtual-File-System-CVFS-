📂 Customised Virtual File System (CVFS)
📌 Project Overview

The Customised Virtual File System (CVFS) is a UNIX-like file system simulation developed using the C programming language. This project mimics the internal working of a traditional operating system file system entirely in memory (RAM), without interacting with actual disk storage.

The main objective of this project is to understand and implement low-level file system mechanisms such as inode management, file descriptor handling, file tables, and system call behavior.

This project demonstrates how operating systems like Linux manage files internally.

🎯 Objectives

To understand the internal structure of a file system.

To simulate system calls like open, close, read, write, etc.

To implement inode-based file management.

To demonstrate file descriptor and file table handling.

To understand permission checking and reference counting.

🛠️ Technologies Used

Programming Language: C

Platform: Linux / Windows (GCC Compiler)

Concepts Used:

Data Structures (Linked List)

Dynamic Memory Allocation

Pointer Management

File Descriptor Table

Inode Structure

System Call Simulation

💻 System Requirements
Hardware Requirements

Minimum 4GB RAM

1 GHz Processor

Software Requirements

GCC Compiler

Linux Terminal / Command Prompt

🏗️ Architecture Components

The project internally maintains the following components:

1️⃣ Superblock

Stores total number of inodes.

Tracks free inodes available in the system.

2️⃣ Inode Structure

Each file is represented using an inode containing:

File name

File size

Actual file size

File type

Permission

Link count

Reference count

Buffer pointer

Next inode pointer

3️⃣ UFDT (User File Descriptor Table)

Maintains file descriptors returned after opening files.

Each entry points to the File Table.

4️⃣ File Table

Stores mode (read/write)

Current offset

Reference count

Pointer to inode

⚙️ Features Implemented

The system supports the following commands:

Command	Description
create	Create new file
open	Open existing file
read	Read file content
write	Write data to file
close	Close opened file
closeall	Close all opened files
ls	List all files
stat	Display file information
fstat	Display file info using descriptor
truncate	Remove file data
rm	Delete file
🔄 Flow of the Project

Initialize Superblock.

Create a linked list of inodes.

Wait for user commands.

Validate input command.

Perform operation:

Allocate inode (if needed)

Update file table

Update offsets

Check permissions

Return output to user.

🧠 Concepts Demonstrated

Inode management

Linked list implementation

Dynamic memory allocation

File descriptor handling

Offset management

Permission validation

Reference counting

UNIX-like system call simulation

🔍 Internal Working of Important System Calls
open()

Checks file existence.

Verifies permission.

Allocates file table entry.

Returns file descriptor.

read()

Validates file descriptor.

Checks read permission.

Reads data from buffer using offset.

Updates read offset.

write()

Validates descriptor.

Checks write permission.

Writes data to file buffer.

Updates write offset.

lseek()

Changes file offset based on:

Start

Current position

End

close()

Decreases reference count.

Frees file table entry if count becomes zero.

📁 How to Compile and Run
gcc cvfs.c -o cvfs
./cvfs
📊 Sample Output
CVFS Started Successfully
cvfs > create Demo 3
File created successfully

cvfs > write Demo
Enter data:
Hello World

cvfs > read Demo 11
Hello World

cvfs > ls
Demo
🚀 Use of This Project

Academic understanding of Operating System concepts.

Practical implementation of file system design.

Interview preparation for system programming roles.

Strengthening C programming and data structure knowledge.

⚠️ Limitations

Works only in memory (data is lost after program termination).

Fixed maximum number of inodes.

No real disk storage interaction.

🔮 Future Improvements

Add disk persistence.

Add directory support.

Implement multi-user access.

Add encryption for file security.

📚 Learning Outcomes

After completing this project, you will understand:

How Linux file systems work internally.

How system calls are implemented.

How file descriptors are managed.

How operating systems handle file security.

👨‍💻 Author

Akash Malgunde
B.E / Information Technology
Project: Customised Virtual File System (CVFS)
