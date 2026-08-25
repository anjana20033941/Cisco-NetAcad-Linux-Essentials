# ⚙️ Types of Linux Commands

Linux executes commands using different mechanisms, including built-in tools, external binaries, shortcuts, and custom functions.

---

## 🔹 1. Internal Commands
Internal commands (also called built-in commands) are built directly into the shell itself. 
* **Example:** The `cd` (change directory) command is part of the Bash shell.
* **Verification:** Use the `type` command to check if a command is built-in.

```bash
type cd
# Output: cd is a shell builtin
🌐 2. External Commands
External commands are binary executables stored in specific directories on the file system. When executed, the shell searches for them within the PATH variable.

Check Command Location: Use the which command to find the absolute path of an executable.

Bash
which ls
# Output: /usr/bin/ls
⚡ 3. Aliases
An alias maps longer or frequently used commands to shorter key sequences. The shell substitutes the full command sequence before execution.

Create an Alias:

Bash
alias name='command'
Example:

Bash
alias ll='ls -la'
🛠️ 4. Functions
Functions group existing commands into a single callable block. They can create new complex utilities or override built-in/external commands.

Syntax:

Bash
function_name () {
    commands
}
