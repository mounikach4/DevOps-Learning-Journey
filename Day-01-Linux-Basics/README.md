# 🐧 Day 1: Introduction to Linux, SDLC Models, and DevOps Basics

Today, I started my DevOps journey by learning the fundamental concepts of Linux, its foundational platforms, software development methodologies, and the role of DevOps.

## 📘 1. What is Linux and What is it Based On?
Linux is an **open-source operating system** that manages a computer's hardware and software resources. 

* **The Unix Foundation:** Linux is **Unix-like**, meaning its architecture and design philosophy are heavily based on **Unix**, a powerful operating system created in the 1970s.
* **The Linux Kernel:** Created by Linus Torvalds in 1991, the kernel interacts directly with your computer hardware. 
* **GNU/Linux:** Most of the daily tools and command-line programs we use are based on the **GNU Project** software utilities combined with the Linux kernel.

### Where and on Which Platforms is Linux Used?
In the DevOps world, you don't always need a physical Linux laptop. Instead, Linux is used on top of these popular platforms:
1. **Cloud Platforms (AWS, Azure, GCP):** Most virtual servers (like AWS EC2 instances) run Linux distributions.
2. **Virtualization Platforms:** Run inside your Windows system using **WSL** (Windows Subsystem for Linux), **VirtualBox**, or VMware.
3. **Container Platforms (Docker, Kubernetes):** Lightweight isolated environments running microservices on top of a Linux base.
4. **Enterprise Distributions:** Packaged into enterprise-ready operating systems like **Ubuntu, Red Hat Enterprise Linux (RHEL), CentOS, and Debian**.

### Why use Linux? (Key Benefits)
* **Open-Source & Free:** Anyone can view, modify, and use the source code without paying licensing fees.
* **High Security:** It is highly resistant to malware, viruses, and unauthorized access.
* **Stability & Performance:** It can run for years without needing a reboot and consumes very few system resources.

---

## 🔄 2. Software Development Methodologies & DevOps

### 📉 Waterfall Model
* **What it is:** A traditional, linear project management approach where development flows sequentially down through distinct phases (Requirements -> Design -> Coding -> Testing -> Deployment).
* **Key Feature:** You cannot move to the next phase until the current phase is completely finished. It is rigid and making changes late in the project is very difficult.

### 🏃 Agile Methodology
* **What it is:** A modern, iterative approach to software development that focuses on continuous feedback and speed.
* **Key Feature:** The project is broken down into small parts called "Sprints" (usually 2-4 weeks). Software is developed, tested, and released in small increments, making it highly adaptable to changes.

### ♾️ What is DevOps?
* **What it is:** DevOps is a combination of cultural philosophies, practices, and tools that increases an organization’s ability to deliver applications quickly.
* **Key Feature:** It bridges the gap between the **Dev**elopment team (who write code) and the **Ops**erations team (who manage servers) to automate testing, deployment, and monitoring, ensuring faster and reliable software delivery.

## Commands Practiced

## 💻 3. Linux Directory Navigation Commands

* **`pwd` (Print Working Directory):** Displays the current folder path you are working in.
* **`ls` (List):** Lists all files and sub-folders in the current directory.
* **`ls -la`:** Shows all files, including hidden files, along with detailed permissions and sizes.
* **`cd [folder_name]` (Change Directory):** Used to move inside a specific folder.
* **`cd ..`:** Moves one step backward to the parent directory.
* **`cd ~`:** Takes you directly to the user's home directory.


## 📁 4. File & Folder Creation

* **`mkdir [folder_name]` (Make Directory):** Creates a brand new folder.
* **`touch [file_name]`:** Creates an empty file quickly.


## 📝 5. Working with File Content

* **`echo "[text]"`:** Prints the specified text right on the screen.
* **`echo "[text]" > file.txt`:** Creates a file and writes the text into it.
* **`cat [file_name]` (Concatenate):** Opens and displays the text/content inside a file.

## 🗑️ 6. File Management & Deletion

* **`mv [old_name] [new_name]` (Move/Rename):** Renames a file or moves it to another location.
* **`rm [file_name]` (Remove):** Deletes a file.
* **`rmdir [folder_name]` (Remove Directory):** Deletes an empty folder.

## ✅ What I Practiced

- Created directories
- Created files
- Added text into files
- Read file contents
- Copied files
- Renamed files
- Deleted files

## 💡 What I Learned

- Linux is case-sensitive.
- Commands should be typed correctly.
- Basic Linux commands are the foundation of DevOps.
  
### 📸 Outputs:

<img width="1920" height="1080" alt="Screenshot 2026-07-10 114240" src="https://github.com/user-attachments/assets/1b3ba098-c987-4176-a2f0-a40c6559f960" />
<img width="1920" height="1080" alt="Screenshot 2026-07-10 114932" src="https://github.com/user-attachments/assets/7b7b072d-8bf9-4e64-8273-c3d8c985d9b6" />
