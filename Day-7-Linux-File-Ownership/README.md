# 🐧 Day 7 - Linux File Ownership

## 🎯 Objective

Learn Linux file ownership, understand the difference between file owner and group owner, and practice changing ownership using chown and chgrp.

## 📘 What is File Ownership?

Every file and directory in Linux has:

- **Owner (User)** – The user who owns the file.
- **Group Owner** – The group associated with the file.

File ownership helps control who can access and manage files, making Linux systems more secure and organized.

## 📘 Why is File Ownership Important?

- Controls access to files and directories.
- Allows secure collaboration between multiple users.
- Prevents unauthorized modifications.
- Plays an important role in Linux system administration.

## 💻 Commands Practiced

### View File Ownership

- Displays file permissions, owner, and group.
ls -l
- Example Output:
-rw-r--r-- 1 root root 0 Jul 16 file.txt

### Change File Owner

- Changes the owner of a file.
chown ram file.txt
- Verify:
ls -l file.txt

### Change Group Ownership

- Changes only the group ownership.
chgrp devops file.txt
- Verify:
ls -l file.txt

### Change Owner and Group Together

- Changes both the owner and group in a single command.
chown dev:linux file1.txt
- Verify:
ls -l file1.txt

### Change Ownership Recursively

- Changes ownership of a directory and all files inside it.
  chown -R krish:aws Ops/
- Verify:
  ls -l Ops

## ✅ What I Practiced

- Created users for ownership practice.
- Created groups for different users.
- Changed the owner of files.
- Changed the group ownership of files.
- Changed both owner and group together.
- Applied recursive ownership changes on a directory.
- Verified all ownership changes using ls -l.

## ❌ Mistakes I Made

### Mistake 1

- Typed: groupdadd linux
- Error: command not found
- Correct Command: groupadd linux

### Mistake 2

- Typed an invalid group creation command with an incorrect group name, which displayed the command usage message.
- Corrected the command and successfully created the required group.

## 💡 Key Learnings

- Every Linux file has an **Owner** and a **Group Owner**.
- chown changes the owner of a file.
- chgrp changes only the group ownership.
- chown owner:group changes both owner and group together.
- chown -R recursively changes ownership for directories and their contents.
- Using ls -l after every command helps verify ownership changes.

## 📸 Outputs

<img width="1920" height="1080" alt="Screenshot 2026-07-16 193225" src="https://github.com/user-attachments/assets/a19d096d-5311-4351-a2ca-7da53c2c5c6a" />
<img width="1920" height="1080" alt="Screenshot 2026-07-16 193241" src="https://github.com/user-attachments/assets/df16d447-e375-463d-baa4-aca4365b1816" />
<img width="1920" height="1080" alt="Screenshot 2026-07-16 193304" src="https://github.com/user-attachments/assets/afd8421d-f271-4f81-b1ec-9b7cebcc7853" />
<img width="1920" height="1080" alt="Screenshot 2026-07-16 193339" src="https://github.com/user-attachments/assets/1c0d36d4-d8fd-4355-a513-1bc7646b30f6" />



