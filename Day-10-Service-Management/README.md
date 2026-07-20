# 🐧 Day 10 - Service Management with systemctl

## 🎯 Objective
Practice controlling Linux services (background programs / daemons) using systemctl — starting, stopping, restarting, checking status, and managing whether a service starts on boot.

**Environment:** AWS EC2 (Amazon Linux 2023)

> A **service** (or daemon) is a program that runs in the background — like a web server or database. systemctl is the tool used to control these services.

## ▶️ Control a Service Now

- Start a service immediately: sudo systemctl start <service>
- Check whether a service is running (plus recent log lines): sudo systemctl status <service>
- Stop a service immediately: sudo systemctl stop <service>
- Restart a service — stops and starts it again (used to apply config changes): sudo systemctl restart <service>

## 🔁 Control Boot Behavior

- Enable a service so it starts automatically on every boot: sudo systemctl enable <service>
- Disable a service so it does NOT start on boot: sudo systemctl disable <service>

## 📋 List Running Services

- Show every service currently running: systemctl list-units --type=service --state=running

## ✅ What I Practiced
- Started and stopped a service using start and stop.
- Checked a service's status and read its recent logs with status.
- Restarted a service to apply configuration changes with restart.
- Enabled a service to auto-start on boot with enable.
- Disabled boot auto-start with disable.
- Listed all running services with list-units.

## 💡 Key Learnings
- **start / stop / restart affect the service RIGHT NOW.** They control the current running state.
- **enable / disable affect the NEXT BOOT.** They control whether the service auto-starts later.
- These two are independent — a service can be **running now but disabled at boot**, or **enabled but currently stopped**.
- status is the go-to debugging command: it shows if a service is active, when it started, and the last few log lines.
- restart is what you run after editing a service's config file, so the new settings take effect.

## 📸 Outputs
