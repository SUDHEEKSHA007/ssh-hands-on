# 🔐 SSH Passwordless Authentication (Linux Hands-on)

> Secure SSH key-based login setup with real-world debugging and configuration

---

## 🔧 Tools Used
- Linux (Ubuntu)
- OpenSSH
- GitHub Codespaces
- Git

---

## 📌 Objective
Set up SSH key-based authentication and connect without password.

---

## 📌 Why This Project
This project demonstrates how secure SSH access is implemented in real-world environments.  
SSH key-based authentication is widely used in cloud platforms to enable secure, passwordless access to servers.

---

## ⚡ Quick Demo

```bash
ssh -p 2222 localhost

✔ Logged into system without password  
✔ SSH running on custom port (2222)
```
---

## ⚙️ Implementation Steps

### 1. Generate SSH Key
```bash
ssh-keygen -t ed25519 -C "test@codespace"
```
### 2. Fix Key Placement (After Incorrect Naming)
Initially, the key was saved with an incorrect name (`ssh localhost`).  
It was corrected using:

```bash
mv ssh\ localhost ~/.ssh/id_ed25519
mv ssh\ localhost.pub ~/.ssh/id_ed25519.pub
---
```
### 3. Set Permissions
To secure the SSH keys, proper file permissions were applied:
```
chmod 700 ~/.ssh
chmod 600 ~/.ssh/id_ed25519
chmod 644 ~/.ssh/id_ed25519.pub
---
```
### 4. Enable SSH Server
Installed and started the OpenSSH server:
```
sudo apt update
sudo apt install -y openssh-server
sudo service ssh start
---
```
### 5. Verify Port
Checked that SSH is running on the custom port (2222):
```
ss -tlnp | grep 2222
---
```
### 6. Connect
Established SSH connection using the configured port:
```
ssh -p 2222 localhost

---
