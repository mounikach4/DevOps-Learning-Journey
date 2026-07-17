# 🐧 Day 8 - SSH Key-Based Login & Root Access

## 🎯 Objective
Set up SSH key-based login for a new user on an EC2 instance, and then grant that user root (sudo) access using the `wheel` group.

**Environment:** AWS EC2 (Amazon Linux 2023)

## 🔑 User Phase — Generate the Key Pair

```bash
ssh-keygen -f <username>
```
Creates two files:
```
<username>        →  private key (stays with user)
<username>.pub    →  public key  (goes to admin)
```

```bash
cat <username>.pub
```
```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAA...  <user>@<host>
```

## 👨‍💻 Admin Phase — Create the User & Add the Key

```bash
sudo su -
useradd <username>
cd /home/<username>
mkdir .ssh
cd .ssh
touch authorized_keys
vim authorized_keys        # paste the user's public key, save
```

## 🔐 Admin Phase — Permissions & Ownership

```bash
chmod 700 .ssh
chmod 600 authorized_keys
chown -R <username>:<group> .ssh
```

Verify:
```bash
ls -la
```
```
drwx------. 2 <username> <group> 29 .ssh
```

> Root creates these files, so root owns them by default. Without `chown -R`, SSH rejects the login.

## 🚪 User Phase — Login with the Private Key

```bash
ssh -i <private_key> <username>@<server-ip>
```
```
[<username>@<hostname> ~]$
```
Logged in — no password prompt.

## 🧑‍🔧 Admin Phase — Grant Root Access

```bash
id <username>
```
```
uid=xxxx(<username>) gid=xxxx(<username>) groups=xxxx(<username>)
```

```bash
usermod -aG wheel <username>
id <username>
```
```
uid=xxxx(<username>) gid=xxxx(<username>) groups=xxxx(<username>),10(wheel)
```

```bash
vim /etc/sudoers            # confirm:  %wheel  ALL=(ALL)  ALL
```


## 🔄 User Phase — Re-login & Test

Group changes apply only to a **new session**:
```bash
exit
ssh -i <private_key> <username>@<server-ip>
```

```bash
sudo useradd <newuser>
id <newuser>
```
```
uid=xxxx(<newuser>) gid=xxxx(<newuser>) groups=xxxx(<newuser>)
```
✅ Root access working.

## ❌ Mistakes I Made

**Mistake 1**
- Typed: cat <username>.pud
- Error: No such file or directory
- Correct: cat <username>.pub

**Mistake 2**
- Typed: ssh -i <username>@<server-ip>
- Error: Warning: Identity file <username>@<server-ip> not accessible: No such file or directory. + full usage dump
- Correct: ssh -i <private_key> <username>@<server-ip>
- -i takes the **key file**. The destination is a separate argument.

**Note on permissions**
- I used chmod 700 authorized_keys and login still worked.
- Convention is 600 for authorized_keys and 700 for .ssh.


## 💡 Key Learnings
- Private key stays with the user; only the public key goes into the server's authorized_keys.
- SSH is strict about ownership — wrong owner = silent Permission denied with no clear reason.
- chown -R is the step that's easiest to forget and hardest to debug.
- wheel group grants sudo on Amazon Linux; /etc/sudoers is where the rule lives.
- Group changes need a fresh session — exit and log back in.
- Read the error message. SSH tells you exactly what's wrong.

## 📸 Outputs

<img width="1920" height="1080" alt="Screenshot 2026-07-17 213357" src="https://github.com/user-attachments/assets/5be7aedf-1f4a-4b62-86ce-3dcab9e5a256" />
<img width="1920" height="1080" alt="Screenshot 2026-07-17 213413" src="https://github.com/user-attachments/assets/e5815fb5-8651-482e-9967-62f961cd1675" />
<img width="1920" height="1080" alt="Screenshot 2026-07-17 213429" src="https://github.com/user-attachments/assets/aa25267a-0ca2-416e-9e47-2280fc582336" />
<img width="1920" height="1080" alt="Screenshot 2026-07-17 213442" src="https://github.com/user-attachments/assets/67faa469-d375-4d6d-8b93-fb8aefebc29b" />
<img width="1920" height="1080" alt="Screenshot 2026-07-17 215428" src="https://github.com/user-attachments/assets/a1316ba9-2163-4966-98be-242e829ea1cf" />
<img width="1920" height="1080" alt="Screenshot 2026-07-17 215448" src="https://github.com/user-attachments/assets/18d4b1d4-e0b4-43d4-9669-de67d4f7c421" />




