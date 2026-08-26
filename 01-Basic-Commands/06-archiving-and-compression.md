# 🗜️ Compression Tools Cheat Sheet (`gzip`, `bzip2`, `xz`, `zip`)

A quick reference for common Linux compression and archiving commands.

---

## 📦 Single-File Compression
*(Replaces the original file)*

| Command | Description |
|---|---|
| `gzip file.txt` | Compresses file to `file.txt.gz` (Lossless) |
| `gunzip file.txt.gz` | Decompresses `file.txt.gz` back to `file.txt` |
| `gzip -l file.txt.gz` | Displays compression ratio and details |
| `bzip2 file.txt` | Higher compression ratio than gzip (uses `.bz2`) |
| `bunzip2 file.txt.bz2` | Decompresses a bzip2 file |
| `xz file.txt` | High compression ratio with fast decompression (uses `.xz`) |

---

## 🗃️ ZIP Archiving
*(Keeps the original files intact)*

| Command | Description |
|---|---|
| `zip archive.zip file1 file2` | Creates a zip archive |
| `zip -r archive.zip directory/` | Recursively zips a directory and its subfolders |
| `unzip archive.zip` | Extracts a zip archive |
| `unzip -l archive.zip` | Lists files inside a zip archive |
| `unzip archive.zip "folder/*"` | Extracts a specific directory's contents from a zip |

---

## 🔑 Useful Key Concepts

### Glob Characters (Wildcards)
| Symbol | Meaning |
|---|---|
| `*` | Matches zero or more characters |
| `?` | Matches exactly one single character |
| `[]` | Matches a range or set of characters |

### Lossless vs. Lossy Compression
- **Lossless** — Restores files to a 100% identical original state. Used for text, documents, code, and software.
- **Lossy** — Permanently discards unnoticeable data to achieve a smaller file size. Used for images, audio, and video.

---

*Compiled as a quick-reference cheat sheet for Linux compression tools.*
