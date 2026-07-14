# 🐧 Day 5: Linux User & Group Management

## 🎯 Objective

Practice Linux user management, group management, and SSH password authentication on an AWS EC2 (Amazon Linux) instance.


# 💻 Commands Practiced

## 👤 User Management

- sudo su -
- useradd lia
- passwd lia
- id lia
- userdel lia

## 👥 Group Management

- groupadd devops
- groupadd linux

- usermod -g devops lia
- usermod -aG linux lia

- groupdel linux
- groupdel devops

## 📄 View User & Group Information

- cat /etc/passwd
- cat /etc/group

## 🔐 SSH Password Authentication

vim /etc/ssh/sshd_config

Update:
- PasswordAuthentication yes

Validate and restart:
- sshd -t
- systemctl restart sshd

# ✅ What I Practiced

- Created and deleted Linux users
- Created and deleted groups
- Changed a user's primary group
- Added a user to a secondary group
- Viewed user and group information
- Enabled SSH password authentication
- Validated SSH configuration
- Restarted the SSH service

# ❌ Mistakes I Made

## Mistake 1: Incorrect `usermod` Command

**Wrong**

usermod -a devops lia

**Correct**

usermod -aG devops lia

## Mistake 2: Weak Password Warning

BAD PASSWORD: The password fails the dictionary check

Although Linux accepted the password, I learned that using a strong password is important for better security.

# 💡 Key Learnings

- Every user has a primary group and can belong to multiple secondary groups.
- usermod -g changes the primary group.
- usermod -aG adds a user to supplementary groups.
- User information is stored in /etc/passwd.
- Group information is stored in /etc/group.
- Always validate SSH configuration using sshd -t before restarting the SSH service.

# 📸 Output

<img width="1920" height="1080" alt="Screenshot 2026-07-14 192105" src="https://github.com/user-attachments/assets/6c1a9e54-f12e-4585-abcf-21c13cfb3c39" />
<img width="1920" height="1080" alt="Screenshot 2026-07-14 192122" src="https://github.com/user-attachments/assets/4a862c41-7c8b-4885-8dd6-f73fa4b01fd8" />
<img width="1920" height="1080" alt="Screenshot 2026-07-14 192143" src="https://github.com/user-attachments/assets/fcc60f6a-c324-4fdd-a80f-0ab2c081ab01" />
<img width="1920" height="1080" alt="Screenshot 2026-07-14 192205" src="https://github.com/user-attachments/assets/a08fa132-16ae-46ca-84f1-0c8b57cf34d2" />
