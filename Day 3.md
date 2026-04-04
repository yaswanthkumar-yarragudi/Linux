# Day 3: Basic Linux Commands 🐧

## Overview
Today we explore the essential Linux commands you'll use every single day as a developer or sysadmin. These commands let you navigate the filesystem, manage files, and understand what's happening on your system.

---

## 1. Navigation Commands

### `pwd` — Print Working Directory
Shows your current location in the filesystem.
```bash
pwd
# Output: /home/username
```

### `ls` — List Directory Contents
```bash
ls            # basic listing
ls -l         # long format (permissions, size, date)
ls -a         # show hidden files (dotfiles)
ls -la        # combine both flags
ls -lh        # human-readable file sizes
```

### `cd` — Change Directory
```bash
cd /home/username     # go to absolute path
cd Documents          # go to relative path
cd ..                 # go up one level
cd ~                  # go to home directory
cd -                  # go back to previous directory
```

---

## 2. File & Directory Management

### `mkdir` — Make Directory
```bash
mkdir myfolder                   # create a folder
mkdir -p projects/linux/day3     # create nested directories
```

### `touch` — Create an Empty File
```bash
touch notes.txt
touch file1.txt file2.txt        # create multiple files
```

### `cp` — Copy Files or Directories
```bash
cp file.txt backup.txt           # copy a file
cp -r myfolder/ newfolder/       # copy a directory recursively
```

### `mv` — Move or Rename
```bash
mv file.txt Documents/           # move file to a folder
mv oldname.txt newname.txt       # rename a file
```

### `rm` — Remove Files or Directories
```bash
rm file.txt                      # delete a file
rm -r myfolder/                  # delete a directory recursively
rm -rf myfolder/                 # force delete (use carefully!)
```

> ⚠️ **Warning:** `rm -rf` is irreversible. Always double-check before running it.

---

## 3. Viewing File Contents

### `cat` — Concatenate & Display
```bash
cat file.txt                     # print file contents
cat file1.txt file2.txt          # print multiple files
```

### `less` — Scrollable File Viewer
```bash
less file.txt
# Use arrow keys to scroll, press q to quit
```

### `head` & `tail` — View Start or End of File
```bash
head file.txt          # first 10 lines
head -n 20 file.txt    # first 20 lines
tail file.txt          # last 10 lines
tail -f logfile.txt    # follow file in real-time (great for logs!)
```

---

## 4. Searching & Finding

### `find` — Search for Files
```bash
find . -name "*.txt"              # find all .txt files in current dir
find /home -name "notes.txt"      # find by name from a path
find . -type d                    # find directories only
```

### `grep` — Search Inside Files
```bash
grep "hello" file.txt             # search for a word
grep -i "hello" file.txt          # case-insensitive
grep -r "error" /var/log/         # search recursively in directory
grep -n "hello" file.txt          # show line numbers
```

---

## 5. System Info Commands

### `whoami` — Current User
```bash
whoami
# Output: username
```

### `uname` — System Information
```bash
uname -a      # all info (kernel, OS, architecture)
```

### `df` — Disk Usage
```bash
df -h         # disk space in human-readable format
```

### `du` — Directory Size
```bash
du -sh myfolder/     # size of a specific folder
```

### `top` / `htop` — Process Monitor
```bash
top            # live system processes (press q to quit)
htop           # improved version (may need installation)
```

---

## 6. Permissions

### `chmod` — Change File Permissions
```bash
chmod 755 script.sh      # rwxr-xr-x
chmod +x script.sh       # add execute permission
chmod -w file.txt        # remove write permission
```

### `chown` — Change File Owner
```bash
chown user:group file.txt
```

### Understanding Permission Notation
```
-rwxr-xr--
 ↑↑↑↑↑↑↑↑↑
 |||||||└─ others: read only
 ||||└──── group: read + execute
 |└─────── owner: read + write + execute
 └──────── file type (- = file, d = directory)
```

---

## 7. Useful Shortcuts & Tips

| Shortcut | Action |
|---|---|
| `Ctrl + C` | Kill running command |
| `Ctrl + Z` | Pause command (send to background) |
| `Ctrl + L` | Clear terminal screen |
| `Tab` | Autocomplete file/command names |
| `↑ / ↓` | Navigate command history |
| `!!` | Repeat last command |
| `man <command>` | Open manual for any command |

---

## 8. Quick Practice Exercises

Try these to reinforce today's learning:

1. Create a directory called `linux-practice` and navigate into it.
2. Create 3 empty files: `file1.txt`, `file2.txt`, `file3.txt`.
3. Write some text into `file1.txt` using `echo "Hello Linux" > file1.txt`.
4. Copy `file1.txt` to `file1-backup.txt`.
5. Search for the word "Hello" inside the file using `grep`.
6. List all files with their sizes in human-readable format.
7. Delete `file3.txt`.

---

## Summary

| Command | Purpose |
|---|---|
| `pwd`, `ls`, `cd` | Navigate the filesystem |
| `mkdir`, `touch`, `cp`, `mv`, `rm` | Manage files and folders |
| `cat`, `less`, `head`, `tail` | View file contents |
| `find`, `grep` | Search files and content |
| `df`, `du`, `top` | Monitor system resources |
| `chmod`, `chown` | Manage permissions |

---

> 📅 **Next up — Day 4:** Text Editors in Linux (Vim, Nano, and more)
