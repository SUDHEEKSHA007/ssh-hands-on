# 🔐 SSH Passwordless Authentication (Linux Hands-on)

## 🔧 Tools Used
- Linux (Ubuntu)
- OpenSSH
- GitHub Codespaces
- Git

---

## Objective
Set up SSH key-based authentication and connect without password.

---

## 📌 Why This Project
This project demonstrates how secure SSH access is implemented in real-world environments. 
SSH key-based authentication is widely used in cloud platforms to enable secure, passwordless access to servers.

---

## ✅ Outcome
- Successfully configured passwordless SSH authentication
- Established secure connection using key-based login
- Debugged real-world issues including port configuration and permissions
- Simulated production-like SSH setup
  
---

## Steps Performed

### 1. Generated SSH Key
```bash
ssh-keygen -t ed25519 -C "test@codespace"
## 🚀 What I Learned
- SSH key-based authentication
- Debugging SSH issues (port, permissions)
- Configuring SSH server
- Fixing GitHub authentication errors (403)
