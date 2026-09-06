# 📄 File Viewing Commands

## `cat`

Displays the entire contents of a text file at once on the standard output.

```bash
cat filename.txt
```

---

## `less`

Opens large files in a scrollable view (pager) to navigate line-by-line or page-by-page.

```bash
less filename.txt
```

### `less` Navigation Keys

Essential shortcuts for moving through files and performing searches inside `less`:

* **Spacebar** : Move one window forward
* **B** : Move one window backward
* **Enter** : Move one line forward
* **/pattern** : Search forward for a specific term or pattern
* **?pattern** : Search backward for a specific term or pattern
* **n** : Jump to the next search match
* **Shift + N** : Jump to the previous search match
* **Q** : Exit `less`
* **H** : Display help screen

---

## `head`

Outputs the beginning portion (default 10 lines) of a file.

```bash
head filename.txt
head -n 5 filename.txt
head -n -5 filename.txt
```

---

## `tail`

Outputs the ending portion (default 10 lines) of a file.

```bash
tail filename.txt
tail -n 5 filename.txt
tail -n +25 filename.txt
tail -f filename.log
```

---

## `|` (Pipe)

Passes the output of one command to serve as the input for the next command.

```bash
ls /etc | head
```

---

## `nl`

Adds line numbers to the standard output.

```bash
ls /etc/ssh | nl | tail -5
```
# 🔁 I/O Redirection & `sort`

## `>` (STDOUT Redirection)

Redirects standard output to a file, overwriting any existing contents of that file.

```bash
echo "Line 1" > example.txt
```

---

## `>>` (Append STDOUT)

Appends standard output to the end of an existing file without overwriting it.

```bash
echo "Another line" >> example.txt
```

---

## `2>` (STDERR Redirection)

Redirects standard error messages to a specified file while leaving standard output unchanged.

```bash
ls /fake /etc/ppp 2> error.txt
```

---

## `&>` (STDOUT and STDERR Redirection)

Redirects both standard output and standard error into the same file.

```bash
ls /fake /etc/ppp &> all.txt
```

---

## Separate Redirection (`>` and `2>`)

Redirects STDOUT and STDERR to two different files simultaneously.

```bash
ls /fake /etc/ppp > example.txt 2> error.txt
```

---

## `<` (STDIN Redirection)

Redirects input from a file into a command instead of taking input from the keyboard.

```bash
tr 'a-z' 'A-Z' < example.txt
```

---

## Combined Input and Output Redirection (`<` and `>`)

Reads input from a file and redirects the resulting output into another file.

```bash
tr 'a-z' 'A-Z' < example.txt > newexample.txt
```

---

## `sort`

Rearranges lines of text based on specified fields and delimiters.

```bash
sort -t: -n -k3 mypasswd
sort -t: -n -r -k3 mypasswd
sort -t, -k2 -k1n -k3 os.csv
```

### `sort` Options

Key flags used to customize sorting rules:

* `-t` : Specifies the field delimiter character (e.g., `-t:` or `-t,`).
* `-k` : Specifies the field number to sort by (starting at 1).
* `-n` : Performs a numerical sort instead of alphabetical.
* `-r` : Reverses the sorting order.
