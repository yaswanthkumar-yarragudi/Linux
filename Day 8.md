# Day 9: Linux Systems Administration
## Disk, Memory, & Networking

This documentation covers the essential commands for monitoring storage, managing system memory, and troubleshooting network configurations.

---

## I. Disk Management
Monitoring disk space is crucial to prevent system hangs caused by full partitions.

### 1. Checking Usage
| Command | Description | Useful Flags |
| :--- | :--- | :--- |
| `df` | **Disk Free**: Shows available space on filesystems. | `df -h` (Human-readable) |
| `du` | **Disk Usage**: Shows size of files/directories. | `du -sh *` (Summary of current dir) |
| `lsblk` | **List Block Devices**: Shows drives and partitions. | `lsblk -p` (Full paths) |

### 2. Management & Mounting
* **`fdisk -l`**: Lists all available disk partitions (requires `sudo`).
* **`mount`**: Attaches a physical disk or partition to a directory in the Linux tree.
    * *Example:* `sudo mount /dev/sdb1 /mnt/data`
* **`umount`**: Detaches a mounted filesystem.

---

## II. Memory (RAM) Management
Linux uses RAM for active processes and "Swap" space on the disk when RAM is full.

### 1. Monitoring Commands
* **`free -h`**: The quickest way to see used/available RAM and Swap in GB/MB.
* **`vmstat`**: Provides a detailed report on virtual memory, paging, and CPU activity.
* **`cat /proc/meminfo`**: Displays raw kernel-level memory statistics.



---

## III. Networking Commands
These tools are used to configure network interfaces and troubleshoot connectivity.

### 1. IP & Interface Configuration
* **`ip addr`**: Shows all network interfaces and their assigned IP addresses.
* **`ip link set <int> up/down`**: Enables or disables a specific network interface.
* **`hostname -I`**: Displays the local IP addresses of the host.

### 2. Troubleshooting Connectivity
* **`ping <host>`**: Checks if a remote server is reachable via ICMP packets.
* **`traceroute <host>`**: Maps the path (hops) a packet takes to reach its destination.
* **`nslookup <domain>`**: Queries DNS servers to find the IP address of a domain name.
* **`curl -I <url>`**: Fetches the HTTP header of a website to test web connectivity.



### 3. Port & Socket Monitoring
* **`ss -tunlp`**: Displays all listening ports and the programs using them.
    * `-t` (TCP), `-u` (UDP), `-n` (Numeric), `-l` (Listening), `-p` (Program).
* **`nmap <ip>`**: Scans for open ports on a target machine (useful for security audits).

---

## IV. Quick Summary Checklist
- [ ] Use `df -h` regularly to monitor disk "Full %".
- [ ] Use `free -h` to check for high "Swap" usage (indicates RAM shortage).
- [ ] Use `ip addr` to confirm your `eth0` or `wlan0` has a valid IP.
- [ ] Use `ss -tunlp` to verify if your web server or database is listening on the correct port.
