# 🐧 Day 11 - Process Management

## 🎯 Objective
Practice Linux process management — listing running processes, understanding PID and PPID, running jobs in the background, monitoring resource usage, and stopping processes safely.

**Environment:** AWS EC2 (Amazon Linux 2023)

> Every command you run becomes a **process**. Each process gets a **PID** (Process ID) and a **PPID** (Parent Process ID — the process that started it). This parent chain runs all the way up to PID 1 (systemd).

## 📋 Listing Processes

- List processes started by the current user: ps
- List every process on the system with full details (UID, PID, PPID, start time, command): ps -ef
- Filter the process list down to a specific program: ps -ef | grep nginx

## ⏳ Foreground vs Background

- **Foreground** – The process blocks the terminal; you can't do anything until it finishes.
- **Background** – The process runs while you keep using the terminal.
- Send a command to the background using &: sleep 10 &

## 📊 Monitoring Resource Usage

- Show a live view of all processes and their CPU / RAM usage: top

## 🛑 Stopping a Process

- Gracefully request a process to shut down (it can clean up first): kill <PID>
- Force a process to stop immediately (last resort): kill -9 <PID>

## ✅ What I Practiced
- Listed processes with ps and ps -ef.
- Read the UID, PID, PPID, and CMD columns to understand process relationships.
- Filtered the process list using ps -ef | grep <name>.
- Ran a command in the background with &.
- Monitored live CPU and RAM usage with top.
- Stopped a process gracefully with kill and forcefully with kill -9.

## 💡 Key Learnings
- Every process has a parent (**PPID**), and Linux tracks who started what, up to PID 1 (systemd).
- The & symbol frees up your terminal — background jobs run without blocking you.
- top is the first place to look when a server feels slow. If a process keeps consuming CPU and RAM without releasing it, that's a signal to check the logs and restart it.
- kill vs kill -9 is a **request vs a demand** — always try a normal kill first so the process shuts down cleanly, and use `-9` only when it won't respond.

## 📸 Outputs

