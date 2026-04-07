# Day 5: File Permissions in Git & GitHub

When working on scripts or automation, Git tracks the **executable bit** of your files. This ensures that a script created on one machine remains runnable when cloned onto another.

---

## 1. Understanding Git File Modes
Git simplifies the standard Linux permission system into specific modes:

| Mode | Type | Description |
| :--- | :--- | :--- |
| **`100644`** | Regular | Standard non-executable file (text, images, code). |
| **`100755`** | Executable | Files that can be "run" (shell scripts, binaries). |

![Git Modes](https://raw.githubusercontent.com/git-guides/git-permissions/main/images/permission-diagram.png)

---

## 2. Common Issues: "Permission Denied"
If you create a script on Windows or with the wrong local settings, it may be committed as `100644`. When a user on Linux or macOS tries to run it, they will see:

`bash: ./script.sh: Permission denied`

![Terminal Error Example](https://cli.re/wp-content/uploads/2020/03/permission-denied.png)

---

## 3. Managing Permissions via Git CLI
You can fix permissions directly in the Git index without relying on your operating system's file explorer.

### Check Current File Modes
To see how Git is currently tracking your file:
```bash
git ls-files --stage
