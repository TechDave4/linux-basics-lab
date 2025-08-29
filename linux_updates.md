# Linux Basics Lab – Notes

### 23/08/25 – Day 1: Shell Basics
- Commands: `echo`, `pwd`, `ls`, `cd`
- Installed a package with `sudo apt install`
- Viewed processes with `htop`

### 24/08/25 – Day 2: Navigation
- Commands: `touch`, `ls -l`, `cat`
- Shortcuts:  
  - `..` → parent directory  
  - `.` → current directory  
  - `~` → home directory  
  - `-` → previous directory  
- Used `clear` to reset terminal

### 25/08/25 – Day 3: Scripting
- Created first Bash script using `nano`
- Scripts must start with a shebang: `#!/bin/bash`
- Made script executable with `chmod +x filename`
- Troubleshooting:  
  - Single quotes `'...'` → literal text  
  - Double quotes `"..."` → variable expansion  
  - `[ ]` requires spaces around operators  
- Practiced loops and conditional statements
- Learned to comment as you script → helps track progress

## 26/08/25 - Day 4: navigating
- Open large files using 'less'
- search for particular events or words in less with ' / '
- to help with reading using less function pair it with '-N' to number lines e.g. ' less -N ***.txt '
trick learnt:
Regex tip: `.` = any single character, `*` = repeat 0 or more times.
Together `.*` = "any number of any characters".
Example: `ERROR:.*Database` matches `ERROR:` followed by anything, then `Database`.
- 'echo' + '>' overwrite, or, '>>' append (add on to existing)
- used 'more' function and evidently the famous joke 'less' is more

### 27/08/25 – Day 5: Exploring
- Practiced navigation between directories with `cd`
- Used `tree` to visualize directory structure (after installing it)
- Tried `du -h` and `df -h` to check file/disk usage
- Learned difference between absolute vs relative paths
- Reminder: always combine exploration with `man command` for built-in help

### 28/08/25 – Day 6: Command Help & Documentation
- Used `history` to review previous commands
- Learned how to copy/move/remove files:  
  - `cp` → copy  
  - `mv` → move/rename  
  - `rm` → remove/delete  
- Explored searching with `find` to locate files
- Practiced command help utilities:  
  - `help command` → quick built-in help (Bash-specific)  
  - `man command` → detailed manual pages (more comprehensive)  
  - `whatis command` → one-line description  
- Learned to create shortcuts with `alias` (e.g., `alias ll='ls -l'`)
- Ended a session properly with `exit` instead of just closing the terminal
- Key takeaway: **don’t memorize everything — know how to look things up efficiently**

### 29/08/25 – Day 7: Permissions & Ownership
- Checked file permissions with `ls -l`  
  - Format: `-rwxr-xr--`  
    - `r` = read, `w` = write, `x` = execute  
    - First group = owner, second = group, third = others
- Changed permissions with `chmod`  
  - Example: `chmod 755 script.sh` → owner can read/write/execute, group & others can read/execute
- Changed file ownership with `chown`  
  - Example: `sudo chown user:user file.txt`
- Explored groups with `groups` and `id`
- Learned symbolic vs numeric modes:  
  - Symbolic: `chmod u+x file.sh` (add execute for user)  
  - Numeric: `chmod 644 file.txt` (rw-r--r--)
- Key takeaway: **permissions are the foundation of Linux security — control who can do what on files and directories**
