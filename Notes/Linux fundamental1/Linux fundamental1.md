# Linux Fundamentals 1 – Notes

## 🌍 Where is Linux Used?

- **Web servers** (websites, web apps)
- **Car systems** (entertainment/control panels)
- **Point of Sale (PoS)** systems
- **Critical infrastructure** (traffic lights, industrial sensors)
- Runs as **servers (Ubuntu)** or **desktop OS**

---

## 🖥️ Basic Commands

| Command       | Meaning                       | Example                |
| ------------- | ----------------------------- | ---------------------- |
| `echo "text"` | Print text (quotes if spaces) | `echo "Hello Friend!"` |
| `whoami`      | Current user                  | `whoami`               |
| `ls`          | List files/folders            | `ls Pictures`          |
| `cd <dir>`    | Change directory              | `cd Pictures`          |
| `cat <file>`  | View file contents            | `cat todo.txt`         |
| `pwd`         | Show current directory        | `pwd`                  |

---

## 🔎 Searching & Finding

- `find -name "*.txt"` → Find all `.txt` files
- `grep "word" file` → Search text inside a file

---

## ⚙️ Operators

| Operator | Description                                            | Example                 |
| -------- | ------------------------------------------------------ | ----------------------- |
| `&`      | Run command in background                              | `cp largefile &`        |
| `&&`     | Run multiple commands (next only if previous succeeds) | `mkdir test && cd test` |
| `>`      | Redirect output (overwrite file)                       | `echo hey > welcome`    |
| `>>`     | Redirect output (append to file)                       | `echo hello >> welcome` |

---

## 💡 Pro Tips

- `ls <dir>` and `cat <path/file>` → No need to `cd` into folder
- Use `find` + `grep` for quick searches
