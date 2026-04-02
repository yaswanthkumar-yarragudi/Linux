# 🚀 DevOps Journey – Day 2: Linux File System Structure

## 📌 What is Linux File System?

The Linux file system is a **hierarchical structure** that organizes files and directories starting from the root directory `/`.

Unlike Windows (C:, D:), Linux uses a **single tree structure**.

---

## 🧭 Linux File System Structure

![Linux File System](https://i.sstatic.net/G9nfJ.png)

👉 Everything starts from `/` (root)

---

## 📂 Important Directories Explained

### 1. `/` (Root Directory)
- The top-most directory  
- All other directories come under this  

---

### 2. `/home`
- User personal directories  
- Example: `/home/yaswanth`  

---

### 3. `/bin`
- Essential user commands  
- Example: `ls`, `cp`, `mv`  

---

### 4. `/sbin`
- System admin commands  
- Example: `reboot`, `fdisk`  

---

### 5. `/etc`
- Configuration files  
- Example: network configs, system settings  

---

### 6. `/var`
- Variable data (logs, cache)  
- Example: `/var/log`  

---

### 7. `/tmp`
- Temporary files  
- Auto-deleted after reboot  

---

### 8. `/usr`
- User programs & applications  
- Contains binaries, libraries, docs  

---

### 9. `/dev`
- Device files  
- Represents hardware (disk, USB)  

---

### 10. `/proc`
- Virtual filesystem  
- Contains system & process info  

---

## 🔥 Key Concept

👉 In Linux:  
**Everything is a file** (even hardware & processes)

