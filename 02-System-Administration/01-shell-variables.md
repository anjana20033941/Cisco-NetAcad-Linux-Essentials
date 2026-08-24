# ⚙️ Linux Shell Variables

Variables store data that can be used by the shell and system processes.

---

## 🔹 1. Local Variables

Local variables exist only within the current shell session and are not accessible by child processes.

**Create/Assign a Local Variable:**
```bash
variable1='Something'
```

**Display Variable Value:**
```bash
echo $variable1
# Output: Something
```

---

## 🌐 2. Environment Variables

Environment variables are available system-wide and accessible by child processes.

**Display an Environment Variable:**
```bash
echo $HISTSIZE
```

**Modify an Existing Variable:**
```bash
HISTSIZE=500
```

**List All Environment Variables:**
```bash
env
```

**Convert Local Variable to Environment Variable:**
```bash
export variable1
```

**Search for a Specific Environment Variable:**
```bash
env | grep variable1
```

**Create and Export in One Step:**
```bash
export variable2='Else'
```

**Remove an Exported Variable:**
```bash
unset variable2
```

---

## 🛣️ 3. PATH Variable

The `PATH` variable defines the directories where the shell looks for executable commands.

**Display Current PATH:**
```bash
echo $PATH
```

**Add Custom Directory to PATH:**
```bash
PATH=/usr/bin/custom:$PATH
```
