# Shell-scripting
**Shell scripting** is the practice of writing a series of commands in a text file (called a *script*) to be executed by the **shell**, which is the command-line interpreter in Unix/Linux systems (like `bash`, `zsh`, etc.).

---

### 🔧 What is a Shell?

A **shell** is a program that lets you interact with the operating system via commands. Common shells include:

- `bash` (Bourne Again SHell) — default in most Linux distros
- `sh`, `zsh`, `ksh`, `fish`, etc.


### ✅ Example of a Shell Script (`example.sh`):

```bash
#!/bin/bash

echo "Hello, $USER!"
echo "Today is $(date)"
```

- `#!/bin/bash` is the *shebang* — tells the system to run the script with `bash`.
- Save it and make it executable:
  ```bash
  chmod +x example.sh
  ./example.sh
  ```

---

### 🔁 Key Features of Shell Scripts

- Variables: `name="Alice"`
- Loops: `for`, `while`
- Conditionals: `if`, `case`
- Functions
- Access to system commands (`ls`, `grep`, `awk`, etc.)

---

### 🧠 Why Use Shell Scripting?

- Lightweight and fast to write
- No need to compile
- Great for automation on Linux systems

---



####  **vim** (Powerful, but steep learning curve)
```bash
vim script.sh
```
- Built-in on nearly every Unix/Linux system
- Advanced editing features
- Use `:syntax on` for highlighting

---

### 🛡️ Notes on **File Permissions in Linux**

In Linux, **file permissions** control who can **read**, **write**, or **execute** files and directories. This is a key part of the system’s security.

---

### 📁 Permission Types

Each file or directory has **three types of permissions** for **three types of users**:

#### **Users:**
1. **Owner** (user)
2. **Group**
3. **Others** (everyone else)

#### **Permissions:**
| Symbol | Meaning  | Applies to |
|--------|----------|------------|
| `r`    | Read     | View contents |
| `w`    | Write    | Modify contents |
| `x`    | Execute  | Run the file (or enter directory) |

---

### 🧾 Example: `ls -l` output

```bash
-rwxr-xr--  1 user group 1234 Apr 28 12:00 script.sh
```

**Breakdown:**

| Section       | Meaning                    |
|---------------|----------------------------|
| `-`           | Type (`-` = file, `d` = dir) |
| `rwx`         | Owner: read, write, execute |
| `r-x`         | Group: read, execute        |
| `r--`         | Others: read only           |

---

### 🔧 Changing Permissions

#### Use `chmod` (change mode):

```bash
chmod u+x file.sh   # Give execute permission to owner
chmod 755 file.sh   # rwxr-xr-x
chmod 644 file.txt  # rw-r--r--
```

#### Use `chown` (change ownership):

```bash
chown username:groupname file.txt
```

---

### 🔢 Numeric (Octal) Permission Representation

| Symbol | Binary | Octal |
|--------|--------|-------|
| `r`    | 4      |       |
| `w`    | 2      |       |
| `x`    | 1      |       |

- So `rwx` = 4+2+1 = **7**
- Example: `chmod 755 file.sh` means:
  - Owner: `7` (rwx)
  - Group: `5` (r-x)
  - Others: `5` (r-x)



---
## My Simple task on Shell Scripting
- creating a file name my_first_shell_script.sh with vim
https://imgur.com/aOQPPsG &
https://imgur.com/zGEpMyQ

- content of the files my_first_shell_script.sh: 
https://imgur.com/THSmwlj

- press key i to allow insert into the file and key esc when done then press :wq to save and exit

- listing the files details inside a directory we will us ls -latr *l - list the files* *a - show hidden files* *t - modified time of the files* *r - reverse the order of the list*

https://imgur.com/jJAVslB

- to run the script you will enter ./ infront of the file that is ./my_first_shell_script.sh then enter. This will give you a permission error to run  
https://imgur.com/QBwVF7q

- You can make the file executable by adding the command chmod +x as this ```chmod +x ./my_first_shell_script.sh```

- creating of 3 folders using mkdir command

https://imgur.com/N0TZw3n

- creation of 3 users using sudo adduser
https://imgur.com/kWLUpEN 
 & https://imgur.com/CxCpuLC

- verifying the user created we use id user(number)
https://imgur.com/OjvmQgg

- A variable is a placeholder, often represented by a symbol like "x" or "y", that can take on different values or represent a quantity that can change.
Declaring a variable and calling the variable using the $ sign at the front. echo is used to print on the shell terminal.
https://imgur.com/Sb56Xhm