# Shell-scripting
*
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

### 🔧 Importance of the Shebang (`#!/bin/bash`) in Shell Scripts

The **shebang** (`#!`) at the top of a script is a **critical directive** that tells the operating system **which interpreter** to use to run the script. It directly affects **how** the script executes.

---

### 🧭 What is a Shebang?

```bash
#!/bin/bash
```

- The `#!` (called *shebang* or *hashbang*) is followed by the **absolute path** to an interpreter.
- In this case, `/bin/bash` tells the system to use the **Bash shell**.

---

### ✅ Why the Shebang is Important

#### 1. **Defines the Interpreter**
- Ensures the script runs with the **intended shell**, regardless of the user’s current shell.
- Example: If a user’s shell is `zsh` or `dash`, but your script uses Bash-specific features, it could break without the correct shebang.

#### 2. **Makes the Script Executable**
- Allows you to run the script directly:
  ```bash
  ./myscript.sh
  ```
  Without the shebang, the system won’t know **how** to run it.

#### 3. **Improves Portability and Predictability**
- Makes scripts behave the same way on different systems.
- Prevents bugs due to shell differences.

---

### 💡 Common Shebang Variants

| Shebang                 | Interpreter Used           |
|-------------------------|-----------------------------|
| `#!/bin/bash`           | Bash shell (standard in Linux) |
| `#!/bin/sh`             | POSIX shell (often `dash` on Ubuntu) |
| `#!/usr/bin/env bash`   | Finds `bash` in system `$PATH` (more portable) |
| `#!/usr/bin/python3`    | Runs a Python script with Python 3 |

---

### ⚠️ What Happens Without a Shebang?

- The script may **fail to run**, or it may run in the **wrong shell**, causing syntax errors.
- You’d have to run it manually with an interpreter:
  ```bash
  bash script.sh
  ```

---

### 🧪 Example:

**script.sh:**
```bash
#!/bin/bash
echo "Hello, world!"
```

Make it executable:

```bash
chmod +x script.sh
./script.sh
```

Output:
```
Hello, world!
```

---

### Summary

The **shebang** is essential in directing how a script is interpreted and executed. It ensures **compatibility**, **correct execution**, and allows scripts to be run as standalone programs.



---
## My Simple task on Shell Scripting

1. creating a folder name shell-script. Shell file is created using. Folders are created using the Mkdir command then the folder name you want. like ``Mkdir shell-script``
https://imgur.com/8nQzJec

2. creating a file name my_first_shell_script.sh with vim, shell file is created using .sh and also we write the shebang at the top of the file this helps the system identify what type of program we running. as for shell script it uses 
``
#!/bin/bash
``
https://imgur.com/SDcaJ8k

3. we get to write into the file. Anaylsing the code: mkdir is used to make a new folder and sudo adduser is used to add a new user
https://imgur.com/MnTtPCg


4. press key esc when done then press. This takes makes us unable to write into the file again then click :wq to save and exit
https://imgur.com/iO7a9zU

5. cd into the folder shell-script
https://imgur.com/r0QPjWy

6. listing the files details inside a directory we will us ls -latr *l - list the files* *a - show hidden files* *t - modified time of the files* *r - reverse the order of the list*
https://imgur.com/9NTMui2

## Running the file

 to run the script you will enter ./ infront of the file that is ./my_first_shell_script.sh then enter. This will give you a permission error to run. This because the file is not giving an execution permission the permission gotten is just read and write 
https://imgur.com/QBwVF7q

1. You can make the file executable by adding the command chmod +x as this ```chmod +x ./my_first_shell_script.sh```
2. then you can run the script now it will work
https://imgur.com/ak1ia4j
3. From the shell file run we are able to created 3 folders. Folder1 Folder2 and Folder3. The command mkdir allows folder to be created. e.g ``mkdir Folder1``
https://imgur.com/3Tfk950

4. We are able to see 3 users created- user1 user2 user3. command id and username will makes us see if there's the user name create. e.g ``id user1``
- user1 https://imgur.com/vUkGMCW
- user2 https://imgur.com/9qngXKQ
- user3 https://imgur.com/mWJcOAZ

5. To validate the Shell file work I rerun the shell file then I got an error that the Folders and user are already existing so there no need to run the program again. except changing the names of the Folders and users then it will created another one.
https://imgur.com/2wOBwwC

## Project value

The function of the script is to easily create a file without having to be writing a command and also create users. The code can be edited to sooth our preference. This enhance fast and efficient method of our work to be automated and fast as a DevOps or system administrator. You can also write this script and send it to another user if you need to help them work on their system so instead of telling them what to enter or name to input you can just write the script and send it to them.