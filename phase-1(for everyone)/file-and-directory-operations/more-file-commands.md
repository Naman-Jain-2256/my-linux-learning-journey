# More File Operations

## Welcome to the Next Level of File Operations! 🚀
In this section, we’ll dive deeper into file management with commands that let you create, copy, move, and rename files like a pro. Get ready to become a file ninja! 🥷

---

## 1. 📄 `cp` – Copy Files and Directories

```bash
cp source_file.txt destination_file.txt          # Copy a file
cp -r source_directory/ destination_directory/   # Copy a directory recursively
cp -i source_file.txt destination_file.txt       # Prompt before overwriting
cp -u source_file.txt destination_file.txt       # Copy only if the source file has a newer modification time than the destination (or if it doesn’t exist)
cp -v source_file.txt destination_file.txt       # Verbose output (show what’s being copied)
```
> 📝 `cp` is your go-to for duplicating files and directories. Use `-r` for recursive copying of directories.
>> Use `-i` to avoid accidental overwrites, and `-v` to see what's happening.

---

## 2. 📦 `mv` – Move or Rename Files and Directories

```bash
mv old_name.txt new_name.txt                       # Rename a file
mv file.txt /path/to/destination/                  # Move a file
mv -i file.txt /path/to/destination/               # Prompt before overwriting
mv -u file.txt /path/to/destination/               # Move only if the source file has a newer modification time than the destination (or if it doesn’t exist)
mv -v file.txt /path/to/destination/               # Verbose output (show what’s being moved)
```
> 📝 `mv` is your tool for moving and renaming files and directories. Use it to keep your file system organized.
>> Use `-i` to prevent accidental overwrites, and `-v` to track the movement process.

---

## 3. 🆕 `touch` – Create Empty Files or Update Timestamps

```bash
touch new_file.txt                # Create an empty file
touch existing_file.txt           # Update the timestamp of an existing file
touch -c non_existent_file.txt    # Do not create if file does not exist
touch -a file.txt                 # Update access time only
touch -m file.txt                 # Update modification time only
```
> 📝 `touch` is like a magic wand for files. Create new ones or update timestamps without opening them.
> Use it to ensure files are fresh or to create placeholders.

---

## 4. 🌳 `tree` – Display Directory Structure

```bash
tree                   # Display the directory structure in a tree format
tree -L 2             # Limit the depth to 2 levels
tree -d                # Show directories only
tree -a                # Show hidden files and directories
tree -h                # Show human-readable file sizes
```
> 📝 `tree` gives you a visual representation of your directory structure. It’s like a map for your file system.
>
> Use it to quickly understand how your files are organized and find what you need.
>
> 💡 You may need to install `tree` with: `sudo apt install tree`

---

## 5. 📑 `cat`, `more`, `less` – View File Contents

```bash
cat file.txt               # Display the entire file contents
more file.txt              # View file contents one screen at a time
less file.txt              # View file contents with backward navigation
cat -n file.txt            # Display line numbers
more -d file.txt           # Show help message for navigation
less -N file.txt           # Show line numbers in less
```
> 📝 These commands let you peek inside files without opening them in an editor. Use `cat` for quick views, `more` for paginated viewing, and `less` for more control.
> 
> Use `cat` for small files, `more` for larger files, and `less` for interactive viewing with navigation.
> 
> 💡 Want to edit after viewing? Try `nano file.txt` to open it in a beginner-friendly terminal editor.

---

## 6. 📋 `stat` – Display File or Directory Status

```bash
stat file.txt                # Show detailed information about a file
stat directory/              # Show detailed information about a directory
stat -c '%n %s %y' file.txt  # Custom format output (name, size, modification time)
stat -f '%N %z %m' directory/ # Custom format for directories
```
> 📝 `stat` provides detailed information about files and directories, including size, permissions, modification time, and more. It’s like a file’s resume.
>
> Use it to check file attributes and understand how your files are structured.
>
> Example output:
```bash
stat -c '%n %s %y' file.txt  
# Output:
# file.txt 4096 2025-07-04 20:30:21
```

---

## 7. 📂 `head`, `tail` - View File Start or End

```bash
head file.txt               # Display the first 10 lines of a file
head -n 5 file.txt          # Display the first 5 lines of a file
tail file.txt               # Display the last 10 lines of a file
tail -n 5 file.txt          # Display the last 5 lines of a file
tail -f file.txt            # Follow a file in real-time
```
> 📝 `head` and `tail` are your go-to commands for quickly viewing the start or end of a file. Use `head` to see the beginning and `tail` to see the end.
>
> Use `-n` to specify the number of lines, and `-f` with `tail` to monitor a file for changes.

---

## 🧠 Bonus Tips
- Use `cp -i` and `mv -i` to avoid accidental overwrites.
- Combine `tree` with `grep` to search for specific files in a directory structure.
- Use `find` for advanced file searching (we’ll cover this in the Searching & Filtering section).
- Use `stat` to check file attributes before copying or moving files.

---

> ## 🏁 Wrap-Up Time: File Artisan Badge Unlocked 🏅
> **Congrats!** You’ve just leveled up your file management skills! 🎉
> 
> **Terminal Level 3** 🕹️ — _Conquered_
>
> From copying and moving files to creating empty placeholders and viewing contents, you now have the tools to handle files like a pro. 🛠️
> 
> ### 🔜 Next Up:
> ➡️ **[Permissions (chmod, chown)](../file-and-directory-operations/permissions.md)** — Master file permissions and ownership to secure your Linux environment! 🔐
> 
> ### 💬 Parting Advice:
> > “Know your files. Name your files. Respect your files.”  
> >
> > _—The Command Line Monk 🧘‍♂️_