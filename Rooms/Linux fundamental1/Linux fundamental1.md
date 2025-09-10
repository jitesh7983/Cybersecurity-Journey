# TryHackMe: Linux Fundamentals 1

**Room Link:** [Linux Fundamentals 1 - TryHackMe](https://tryhackme.com/room/linuxfundamentals1)  
**Difficulty:** Easy  
**Category:** Linux / Fundamentals  
**Completion Date:** Sept 10, 2025

---

## Overview

This room introduced me to the **basics of Linux**, including navigating the filesystem, working with files and directories, searching files, and using operators. I practiced commands like `ls`, `cd`, `cat`, `pwd`, and learned how to manipulate file contents and run commands efficiently.

---

## Key Learnings

- **Linux Usage:**

  - Powers **web servers, PoS systems, cars, traffic lights, industrial sensors**
  - Can run as **desktop OS** or **server (Ubuntu)**

- **Basic Commands:**

| Command       | Meaning                       | Example                |
| ------------- | ----------------------------- | ---------------------- |
| `echo "text"` | Print text (quotes if spaces) | `echo "Hello Friend!"` |
| `whoami`      | Current user                  | `whoami`               |
| `ls`          | List files/folders            | `ls Pictures`          |
| `cd <dir>`    | Change directory              | `cd Pictures`          |
| `cat <file>`  | View file contents            | `cat todo.txt`         |
| `pwd`         | Show current directory        | `pwd`                  |

- **Searching & Finding:**

  - `find -name "*.txt"` → Find all `.txt` files in current directory
  - `grep "word" file` → Search text inside files

- **Operators:**

| Operator | Description                                                 | Example                        |
| -------- | ----------------------------------------------------------- | ------------------------------ |
| `&`      | Run command in background                                   | `cp largefile &`               |
| `&&`     | Run multiple commands (next runs only if previous succeeds) | `mkdir test && cd test`        |
| `>`      | Redirect output (overwrite file)                            | `echo password123 > passwords` |
| `>>`     | Redirect output (append to file)                            | `echo tryhackme >> passwords`  |

---

## Practical Tasks and Commands

| Task                                                    | Command                        |
| ------------------------------------------------------- | ------------------------------ |
| Run a command in the background                         | `command &`                    |
| Replace contents of file `passwords` with `password123` | `echo password123 > passwords` |
| Append `tryhackme` to file `passwords`                  | `echo tryhackme >> passwords`  |

---

### Example Commands

```bash
# Print text
echo "Hello Friend!"

# Find all txt files
find -name "*.txt"

# Search inside a file
grep "tryhackme" passwords

# Run command in background
cp largefile &

# Multiple commands in sequence
mkdir test && cd test

# Redirect output
echo password123 > passwords
echo tryhackme >> passwords
```

# completion proof

![Completion Image](images/Linux1.png)
