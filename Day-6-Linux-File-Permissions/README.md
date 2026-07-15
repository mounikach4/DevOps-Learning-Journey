# 🐧 Day 6 - Linux File Permissions & SSH

## 🎯 Objective

Learn Linux file permissions, understand symbolic and numeric permission modes, practice the `chmod` command, and verify SSH login using a different Linux user.

## 📘 What are Linux File Permissions?

Linux file permissions determine who can access a file or directory and what actions they can perform.

There are three basic permissions:

- **Read (r)** – Allows viewing the contents of a file.
- **Write (w)** – Allows modifying the file.
- **Execute (x)** – Allows executing a file as a program or script.

Permissions are assigned to:

- **User (Owner)**
- **Group**
- **Others**

## 📘 Permission Values

Permission - Symbol - Value 
- Read       -  r     -  4 
- Write      -  w     -  2 
- Execute    -  x     -  1 

Example:
- 7 = rwx
- 6 = rw-
- 5 = r-x
- 4 = r--
- 3 = -wx
- 2 = -w-
- 1 = --x
- 0 = ---

## 📘 What is chmod?

chmod (Change Mode) is a Linux command used to change file and directory permissions.

It supports two methods:

- **Symbolic Mode**
- **Numeric Mode**

## 🔐 What is SSH?

- SSH (Secure Shell) is a secure protocol used to remotely connect and manage Linux servers.
  
# 💻 Commands Practiced

### View File Permissions
- ls -l
  
Displays detailed file information, including permissions.

### Add Write Permission to Group
- chmod g+w file.txt

Adds write permission for the group.

### Give Full Permission to User
- chmod u+rwx file1.txt
  
Grants read, write, and execute permissions to the owner.

### Give Full Permission to Group and Others
- chmod go+rwx file1.txt
  
Grants read, write, and execute permissions to both group and others.

### Remove Write and Execute Permission from Group
- chmod g-wx file1.txt
  
Removes write and execute permissions from the group.

### Remove Write and Execute Permission from Others
- chmod o-wx file1.txt
  
Removes write and execute permissions from others.

### Give Full Permission to Everyone
- chmod ugo+rwx file1.txt
  
Grants full permissions to User, Group, and Others.

### Numeric Permission Example
- chmod 744 file2.txt
  
Permission becomes: rwxr--r--

### Numeric Permission Example
- chmod 344 file.txt
  
Permission becomes: -wxr--r--

### SSH Login
- ssh <username>@<public-ip>

Logs into the remote Linux server securely.

## ✅ What I Practiced

- Created sample files
- Viewed file permissions using ls -l
- Added permissions using symbolic mode
- Removed permissions using symbolic mode
- Assigned permissions using numeric mode
- Verified permission changes
- Logged into the EC2 instance using SSH with another Linux user

## ❌ Mistakes I Made

- Initially, I found numeric permissions like **744** and **344** confusing.
- I wasn't able to understand how Linux converts numbers into permissions.
- After practicing multiple examples and verifying them using ls -l, I understood how permission values are calculated.

## 💡 Key Learnings

- Linux permissions are assigned to **User, Group, and Others**.
- Read = **4**, Write = **2**, Execute = **1**.
- chmod supports both symbolic and numeric permission modes.
- ls -l is useful for verifying permission changes.
- SSH allows secure remote access to Linux servers.
- Practicing permission changes helped me understand Linux security fundamentals.

## 📸 Outputs

<img width="1920" height="1080" alt="Screenshot 2026-07-15 194806" src="https://github.com/user-attachments/assets/917a77c5-f483-443e-9315-845ea8b0a8b1" />
<img width="1920" height="1080" alt="Screenshot 2026-07-15 195621" src="https://github.com/user-attachments/assets/15b5131b-4e1c-4ab5-9261-c0f285f15076" />
<img width="1920" height="1080" alt="Screenshot 2026-07-15 200035" src="https://github.com/user-attachments/assets/87bb972f-46c3-4c14-adc2-4ca9e014c501" />
