# Shell-scripting
**Shell scripting** is the practice of writing a series of commands in a text file (called a *script*) to be executed by the **shell**, which is the command-line interpreter in Unix/Linux systems (like `bash`, `zsh`, etc.).

---

### 🔧 What is a Shell?

A **shell** is a program that lets you interact with the operating system via commands. Common shells include:

- `bash` (Bourne Again SHell) — default in most Linux distros
- `sh`, `zsh`, `ksh`, `fish`, etc.

---

### 📝 What Is a Shell Script?

A **shell script** is a file containing commands you'd normally run in a terminal — used for:

- Automating repetitive tasks
- System administration (backups, user management)
- Installing software or updates
- Startup routines and deployment
- Writing quick utilities

---

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


### 🔧 Common Editors for Writing Shell Scripts

#### 1. **nano** (Beginner-friendly)
```bash
nano script.sh
```
- Simple, built-in on most distros
- On-screen shortcuts
- Good for quick edits

---

#### 2. **vim** or **vi** (Powerful, but steep learning curve)
```bash
vim script.sh
```
- Built-in on nearly every Unix/Linux system
- Advanced editing features
- Use `:syntax on` for highlighting

---

#### 3. **gedit** (GUI editor for GNOME)
```bash
gedit script.sh
```
- User-friendly graphical editor
- Syntax highlighting for shell scripts

---

#### 4. **Visual Studio Code (VS Code)** ⭐ Recommended for productivity
- With extensions like **ShellCheck** and **Bash IDE**
- Linting, debugging, autocomplete

---

#### 5. **Sublime Text / Atom / Notepad++ (Windows)**
- Cross-platform GUI editors
- Plugin support for shell scripting


---
## My Simple task on Shell Scripting
- using vim to input some command on a file name my_first_shell_script.sh

https://imgur.com/aOQPPsG

- content of the files my_first_shell_script.sh: 
https://imgur.com/THSmwlj
- press key i to allow insert into the file and key esc when done then press :wq to save and exit

- to run the script you will enter ./ infront of the file that is ./my_first_shell_script.sh then enter. This will give you a permission error to run  
https://imgur.com/QBwVF7q

- You can make the file executable by adding the command chmod +x as this ```chmod +x ./my_first_shell_script.sh```

- creating of 3 folders using mkdir command

https://imgur.com/N0TZw3n

- creation of 3 users using sudo adduser
https://imgur.com/kWLUpEN 
 & https://imgur.com/CxCpuLC

- verifying the user created we use id nameoftheuser
https://imgur.com/vsp2fhX

- Declaring a variable and calling the variable using the $ sign at the front
https://imgur.com/Sb56Xhm