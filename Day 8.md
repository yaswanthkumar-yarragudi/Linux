# Shell Scripting Basics (for Markdown Automation)

In shell scripting, everything is treated as **text or a command**.  
You can use basic logic to automate repetitive tasks like creating files or checking for updates.

---

## 🔹 1. Variables
Variables store information you want to reuse.
⚠️ Note: No spaces around `=` sign.

```bash
name="Gemini"
version="1.0.0"

echo "Project: $name"
echo "Version: $version"
```

---

## 🔹 2. Conditional Statements (if)
The `if` statement checks if a condition is true.

```bash
# -f checks if a file exists
if [ -f "README.md" ]; then
    echo "Documentation already exists."
else
    echo "# New Project" > README.md
    echo "File created successfully."
fi
```

### Common Logic Symbols

| Symbol | Meaning |
|--------|--------|
| -f     | File exists |
| -d     | Directory exists |
| -eq    | Equal to (numbers) |
| ==     | Equal to (text) |

---

## 🔹 3. For Loops
Loops help perform repetitive tasks.

```bash
# Add timestamp to all Markdown files
for file in *.md; do
    echo "Last updated: $(date)" >> "$file"
    echo "Updated $file"
done
```

---

## 🔹 4. User Input (read)
Use `read` to take input from users.

```bash
echo "Enter the document title:"
read doc_title

echo "# $doc_title" > manual.md
echo "Manual for $doc_title generated."
```

---

## 🔹 5. Simple Math
Basic arithmetic using `$(( ))`.

```bash
count=5
total=$((count + 10))

echo "Total pages: $total"
```

---

## 🔹 Summary Script

```bash
#!/bin/bash

folder="docs"

# 1. Check if folder exists
if [ ! -d "$folder" ]; then
    mkdir "$folder"
fi

# 2. Create multiple files
for i in 1 2 3; do
    echo "# Document Part $i" > "$folder/part_$i.md"
done

echo "Simple documentation structure created in /$folder"
```

---
