# 🐧 Day 9 - Package Management

## 🎯 Objective
Practice the core dnf package management commands on Amazon Linux — installing, removing, updating, listing, searching, and tracking package history.

**Environment:** AWS EC2 (Amazon Linux 2023)

## 📦 Install & Remove

- Install a package (dnf pulls in all required dependencies): sudo dnf install <package>
- Remove a package (also removes packages that depend on it): sudo dnf remove <package>
## 🔄 Update & Upgrade

- Update all installed packages to their latest available version: sudo dnf update

- Upgrade all packages — same result: sudo dnf upgrade

> On this system dnf update is an **alias** for dnf upgrade. Both bring every package to its latest version.

## 📋 List & Search

- List every package installed on the system: dnf list installed
- List every package available to install from the repos: dnf list available
- Count how many packages are available: dnf list available | wc -l
- Search for a package by keyword (when you don't know the exact name): dnf search <keyword>

## 🕓 History

- View a full log of every install, update, and removal: dnf history

## ✅ What I Practiced
- Installed a package and watched dnf resolve its dependencies automatically.
- Removed a package along with its dependents.
- Ran dnf update and dnf upgrade and confirmed they do the same thing.
- Listed installed packages with dnf list installed.
- Listed available packages with dnf list available.
- Counted available packages by piping into wc -l.
- Searched for packages by keyword using dnf search.
- Reviewed the transaction log with dnf history.

## 💡 Key Learnings
- **dnf resolves dependencies for you** — install one package and it fetches everything that package needs.
- **update = upgrade** — on this system, update is just an alias for upgrade.
- **dnf list available | wc -l** is a clean way to see how many packages the repos actually offer.
- **dnf search** is the go-to command, since you rarely remember exact package names.
- **dnf history** is an audit trail — every change is logged, which makes debugging a broken system much easier.
- Commands that change the system (install, remove, update) need sudo; read-only ones (list, search, history) don't.

## 📸 Outputs

<img width="1920" height="1080" alt="Screenshot 2026-07-18 205500" src="https://github.com/user-attachments/assets/14068c54-4eb2-4917-87f5-8211dc77f51f" />
<img width="1920" height="1080" alt="Screenshot 2026-07-18 205716" src="https://github.com/user-attachments/assets/5a80f43f-f552-4376-a78b-09ee79371c24" />

