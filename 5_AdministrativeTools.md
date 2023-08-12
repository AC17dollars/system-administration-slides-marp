---
marp: true
paginate: true
author: Abhinav Chalise, Saugat Neupane
headingDivider: 2
footer: 2023-08-13
header: Abhinav Chalise, Saugat Neupane
---

# Administrative Tools

# AWK Tool

## Introduction

The AWK tool is a versatile programming language used for text processing and data extraction. It is essential for system administrators due to its powerful text manipulation capabilities.

## Why is AWK Required by System Administrators?

System administrators often need to process and extract information from log files, configuration files, and system outputs. AWK provides a concise way to perform these tasks efficiently.

## What Does AWK Do?

AWK scans input files line by line and allows you to define patterns and actions to be performed on matching lines. It's commonly used for text searching, filtering, and data extraction.

### Examples

Search for lines containing "error" in a log file and print them:

```bash
awk '/error/ {print}' logfile.txt
```

Extract and print the second field from a CSV file:

```bash
awk -F ',' '{print $2}' data.csv
```

# Search

## Introduction

Searching is required by system administrators to locate files, directories, and specific content within files.

## Why is Searching Required?

System administrators often need to find configuration files, logs, or specific data within files to troubleshoot issues and maintain the system.

## Searching for Files and Directories

Use the `find` command to search for files and directories based on various criteria. For example, to find all `.log` files in the `/var/log` directory:

```bash
find /var/log -name "*.log"
```

## Searching Within a File

To search for specific text within files, use tools like `grep` and `sed`. For instance, to find lines containing "error" in a file:

```bash
grep "error" logfile.txt
```

# Sort Tools

## Introduction

Sort tools are necessary for system administrators to organize and analyze data efficiently.

## Examples of Sort Tools

Tools like `uniq`, and `sort` commands in Unix-like systems help in sorting and filtering data.

## Why Are Sort Tools Required?

Sort tools assist in arranging data in a meaningful order, which is essential for analyzing logs, reports, and other data.

## Sorting Files by Name, Date, etc.

To sort files by name or date, use the `ls` command with appropriate options. For example, to list files in the current directory by modification date:

```bash
ls -lt
```

## Sorting Contents of Files

To sort the contents of a file, use the `sort` command. To sort lines in a text file:

```bash
sort file.txt
```

# Shell Scripts

## Introduction

Shell scripting involves writing sequences of commands to automate tasks and perform various system operations.

## What is Scripting?

Scripting is the process of creating executable files containing a series of commands that the system can execute.

## Most Commonly Used Shell

Bash (Bourne Again Shell) is the most commonly used shell for scripting due to its availability on most Unix-like systems.

## Basics of Bash Scripting

Scripts start with a shebang (`#!/bin/bash`) followed by commands. They can include variables, loops, conditions, and functions.

### Example: Simple Backup Script

```bash
#!/bin/bash
backup_dir="/backup"
source_dir="/data"

cp -r $source_dir $backup_dir
echo "Backup completed!"
```

## Other Types of Scripting

In addition to shell scripting, Python, Perl, and Ruby are commonly used scripting languages for various tasks.

# Make Tool

## Introduction

The `make` tool is used for building and managing projects, especially compiling source code.

## Why is Make Tool Required?

System administrators use the `make` tool to automate the compilation and building of software projects.

## What Does Make Tool Do?

`make` reads a `Makefile` that specifies how to derive the target program from its source files.

## Examples: Compiling Source Using Make

Suppose you have a C program `hello.c` and a `Makefile` like this:

```make
hello: hello.c
    gcc -o hello hello.c
```

Run `make` in the same directory:

```bash
make
```

This compiles `hello.c` and produces an executable named `hello`.

## Makefile Example

```make
CC = gcc
CFLAGS = -Wall

all: program

program: main.c functions.c
    $(CC) $(CFLAGS) -o program main.c functions.c
```

In this example, `make all` compiles `main.c` and `functions.c` into an executable `program`.

# Thank You
