# Day 4: Linux File Operations

This chapter focuses on the essential commands for managing files and directories within the Linux terminal.

---

## 1. Creating Files and Directories
The first step in file management is knowing how to generate new assets.

### `touch`
Used to create an empty file or update the timestamp of an existing one.
* **Usage:** `touch <filename>`
* **Example:** `touch index.html`

### `mkdir`
Creates a new directory.
* **Usage:** `mkdir <directory_name>`
* **Recursive Creation:** Use `mkdir -p` to create nested folders (e.g., `mkdir -p src/assets/images`).

![Folder Icon](https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Folder.png)

---

## 2. Moving and Renaming (`mv`)
In Linux, the `mv` command serves a dual purpose: relocating files and changing their names.

| Operation | Command Example |
| :--- | :--- |
| **Move** | `mv script.sh ./scripts/` |
| **Rename** | `mv old_name.txt new_name.txt` |

---

## 3. Copying Data (`cp`)
To duplicate files or directories, use the `cp` command.

* **Files:** `cp source.txt destination.txt`
* **Directories:** You **must** use the `-r` (recursive) flag to copy folders.
  * *Example:* `cp -r backup/ backup_final/`

![Clipboard Icon](https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Clipboard.png)

---

## 4. Deleting Files and Folders (`rm`)
**Warning:** Deletion in Linux is permanent. There is no "Recycle Bin."

* **`rm <file>`**: Deletes a single file.
* **`rm -r <dir>`**: Deletes a directory and its entire contents.
* **`rm -rf`**: Forces deletion without any confirmation prompts.

![Warning Icon](https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Symbols/Warning.png)

---

## 5. Viewing File Contents
Quickly inspect files without opening a full text editor.

1.  **`cat`**: Dumps the entire file content into the terminal.
2.  **`less`**: Opens a scrollable view (useful for large files).
3.  **`head` / `tail`**: View the first or last 10 lines of a file.
4.  **`tail -f`**: Monitors a file in real-time as it updates (standard for log monitoring).

---

### Quick Reference Summary

| Command | Action | Key Flag |
| :--- | :--- | :--- |
| `touch` | Create File | N/A |
| `mkdir` | Create Folder | `-p` |
| `mv` | Move/Rename | N/A |
| `cp` | Copy | `-r` |
| `rm` | Remove | `-f` |
