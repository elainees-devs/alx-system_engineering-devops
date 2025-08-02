Here’s a sample `README.md` for your project task:

---

## 0x03. Shell, init files, variables and expansions

### Task: **0. <span style="color:green">Alias</span>**

#### **Objective**

Create a script that defines a shell alias.

#### **Requirements**

* **Alias name:** `ls`
* **Alias value:** `rm *`
* This means running `ls` will delete all files in the current directory.

#### **File**

* `0-alias`

#### **Example Usage**

```bash
julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2

julien@ubuntu:/tmp/0x03$ source ./0-alias

julien@ubuntu:/tmp/0x03$ ls
# All files are deleted

julien@ubuntu:/tmp/0x03$ \ls
# Still shows files using the real `ls` command (escaped with backslash)
```

#### **Directory Structure**

```
alx-system_engineering-devops/
└── 0x03-shell_variables_expansions/
    └── 0-alias
```

#### **How to Use**

```bash
source 0-alias
ls   # This will run rm * due to alias
```

---

