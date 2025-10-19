+++
date = '2025-10-19'
draft = true
title = 'Weekly Cybersecurity Blog'
+++

# Week 1 - Linux Basics for Cybersecurity (My Learning Log)

I'm starting to document my cybersecurity learning journey. I'm currently in Course 4 of the Google Cybersecurity Professional Certificate, and this week I began working with Linux - one of the core tools used in security operations, incident response, forensics, and ethical hacking.

---

## Why Linux Matters in Cybersecurity

Most servers and security tools run on Linux. If you want to: 
- Investigate logs
- Manage systems
- Run penetration testing tools
- Analyze malware or incidents

...you **must** be comfortable with the terminal.

---

## Commands I Learned This Week

### 1) Navigating the File System

```bash
pwd          # Show current working directory
ls -la       # List all files including hidden ones and shows properties: permissions, ownership, size, modification date
cd /path     # Move into a directory
cd ..        # Go up one level
```

---

### 2) Creating and Managing Files & Directories

```bash
touch file.txt             # Create a blank file
nano file.txt              # Create and edit a file using nano editor
mkdir folder_name          # Create a directory
mv file.txt /path/to/dir/  # Move a file to a different location
cp file.txt /path/to/dir/  # Copy a file
rm file.txt                # Delete a file
rm -r folder_name          # Delete a folder and all its contents recursively
```

> **Warning:** Never use 'rm -rf /' or 'sudo rm -rf *' - this deletes your entire system.

---

### 3) Searching & Filtering

```bash
grep "word" filename       # Search for a specific string inside a file
ls -l | grep ".txt"        # Pipe output of ls -l to grep to find .txt files
find /path -name "file_name"  # Find files/directories by name
# find options:
# -iname : case-insensitive name search
# -mtime : modified N days ago
# -mmin  : modified N minutes ago
```

---

### 4) Permissions

- **Types:** read ('r'), write ('w'), execute ('x')  
- **Owners:** user ('u'), group ('g'), others ('o')  

```bash
chmod u+x file.txt         # Add execution permission for user
chmod g-w file.txt         # Remove write permission from group
```

---

### 5) User & Group Management

```bash
useradd -g primary_group -G supplemental_group username  # Add a new user with primary and supplemental groups
usermod -a -G groupname username                        # Append a supplemental group to an existing user
userdel username                                        # Delete a user
```

---

### 6) Changing Ownership

```bash
chown user:group file.txt  # Change owner and group of a file or directory
```

---

### Notes

- Linux commands are **case-sensitive**.
- Use the 'man' command for details: 'man command_name'
- Practice these commands in a terminal; this will solidify your understanding.

---

### Reflection

Learning Linux commands is similar to learning any programming or scripting language - it cannot be memorized and must be regularly practiced. Writing down these commands helped me keep a record of what each one does and how it is used.

### What's Next?

Next, I will start learning SQL and document it in my following post.
