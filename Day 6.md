# Day 7: Linux Systems Administration
## Package Management & Process Management

### 1. Package Management
Package managers automate the installation, configuration, and removal of software. Tools vary by the Linux distribution "family."

#### Debian/Ubuntu Family (using APT)
* **Update Database:** `sudo apt update` (Updates the list of available packages).
* **Upgrade Software:** `sudo apt upgrade` (Installs newer versions of existing packages).
* **Install Package:** `sudo apt install <package_name>`
* **Remove Package:** `sudo apt remove <package_name>`
* **Search for Package:** `apt search <keyword>`

#### Red Hat/Fedora Family (using DNF)
* **Install Package:** `sudo dnf install <package_name>`
* **Remove Package:** `sudo dnf remove <package_name>`
* **Check for Updates:** `sudo dnf check-update`

---

### 2. Process Management
A process is a running instance of a program identified by a **PID** (Process ID).

#### Monitoring Tools
* `ps aux`: Snapshot of all running processes.
* `top`: Real-time interactive view of system resource usage.
* `htop`: An advanced, user-friendly version of `top` (interactive and color-coded).

#### Terminating Processes
* `kill <PID>`: Gracefully requests a process to stop (SIGTERM).
* `kill -9 <PID>`: Forces a process to stop immediately (SIGKILL).
* `pkill <process_name>`: Kills processes based on their name.

---

### 3. Job Control (Foreground & Background)
Manage tasks within your current terminal session.

| Command | Action |
| :--- | :--- |
| `command &` | Runs the command in the background immediately. |
| `Ctrl + Z` | Pauses a running foreground process and moves it to background. |
| `jobs` | Lists all background jobs in the current session. |
| `fg %<n>` | Brings job number `n` to the foreground. |
| `bg %<n>` | Resumes a paused background job. |
| `Ctrl + C` | Terminates the current foreground process. |

---

### 4. Summary Checklist
- [ ] Run `sudo apt update` before installing new tools.
- [ ] Identify high-resource processes using `htop`.
- [ ] Use `grep` with `ps` to find specific PIDs: `ps aux | grep <name>`.
- [ ] Use `kill -9` only if a standard `kill` fails.
