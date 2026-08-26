🗜️ Compression Tools (gzip, bzip2, xz, zip)

📦 Single-File Compression (Replaces original file)

gzip file.txt → Compresses file to file.txt.gz (Lossless).
gunzip file.txt.gz → Decompresses file.txt.gz back to file.txt.
gzip -l file.txt.gz → Displays compression ratio and details.
bzip2 file.txt → Higher compression ratio than gzip (Uses .bz2).
bunzip2 file.txt.bz2 → Decompresses bzip2 file.
xz file.txt → High compression ratio with fast decompression (Uses .xz).

🗃️ ZIP Archiving (Keeps original files)

zip archive.zip file1 file2 → Creates a zip archive.
zip -r archive.zip directory/ → Recursively zip a directory and subfolders.
unzip archive.zip → Extract zip archive.
unzip -l archive.zip → List files inside a zip archive.
unzip archive.zip "folder/*" → Extract specific directory contents from zip.

4. Useful Key Concepts
5. 
Glob Characters (Wildcards):
* : Matches zero or more characters.
? : Matches exactly one single character.
[] : Matches a range or set of characters.

Lossless vs. Lossy Compression:

Lossless: Restores files to 100% identical original state (Used for text, docs, code, software).
Lossy: Permanently discards unnoticeable data for smaller file size (Used for images, audio, video).
