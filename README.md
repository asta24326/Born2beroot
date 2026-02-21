*This project has been created as part of the 42 curriculum by asharafe.*

# 🖥️ Born2beRoot

### ✅ Result: 100/100

## 📄 Description
Born2beRoot is a System Administration project that introduces the fundamentals of virtualization. The goal is to set up a first server using Debian (or Rocky Linux) in a virtual machine, implementing strict security rules. This project covers partitioning with LVM, managing users and groups, configuring sudo, SSH, a strong password policy, and a custom monitoring script.



---

## 🎯 Acquired Skills
* **Virtualization**: Creating and configuring a virtual machine using VirtualBox or UTM.
* **OS Installation**: Installing a CLI-based Linux distribution (Debian/Rocky).
* **Security & Polices**: Implementing a strict password policy (UFA) and configuring a firewall (UFW).
* **System Monitoring**: Writing a Bash script to monitor system resource usage and broadcast it to all users.
* **LVM (Logical Volume Management)**: Setting up a dynamic and secure partitioning system.
* **SSH Configuration**: Setting up secure remote access via a specific port and disabling root login.

---

## 🛠 Contents
The project requires the setup of several services and configurations:
1. **Sudo**: Strict configuration including log paths and custom error messages.
2. **SSH**: Running on port 4242 with root access disabled.
3. **UFW**: Firewall enabled, allowing only the SSH port.
4. **Monitoring Script**: A script that displays system info (CPU, RAM, Disk, etc.) every 10 minutes using `wall`.
5. **Bonus Part**: Setting up a functional WordPress site with Lighttpd, MariaDB, and PHP, plus an additional service (e.g., FTP or Fail2Ban).



---

## ⚙️ Setup & Requirements
The project follows specific system requirements:
* **Operating System**: Debian 12 (latest stable) or Rocky Linux.
* **Partitioning**: At least two encrypted partitions using LVM.
* **Encryption**: The root partition must be encrypted.
* **Hostname**: The hostname must end with `42` (e.g., `asharafe42`).

To check the signature of your virtual machine:
```bash
shasum Born2beRoot.vdi

```

---

## 🧪 How to Use

Since this is a virtual machine project, interaction happens via the terminal.

1. **Accessing the server**:
Connect via SSH from your host machine:

```bash
ssh asharafe@localhost -p 4242

```

2. **Checking the Monitoring Script**:
Wait for the broadcast or run it manually:

```bash
sudo /usr/local/bin/monitoring.sh

```

3. **Verifying Services**:
Check the status of UFW or AppArmor:

```bash
sudo ufw status
sudo aa-status

```

---

## 💡 AI Usage

AI tools were used during the development of this project for:

* **Documentation**: Formatting the README to match the established gold standard for 42 projects.
* **Scripting**: Debugging the `awk` and `grep` commands used in the monitoring script.
* **Concept Clarification**: Understanding the difference between LVM and standard partitioning, and how AppArmor enhances security.
* *Note: The entire server configuration and script logic were implemented manually to pass the live defense.*

---

## 🔗 Resources

* 42 Project Subject: Born2beRoot.
* [Debian Security Guide](https://www.google.com/search?q=https://www.debian.org/doc/manuals/debian-handbook/security.en.html).
* [LVM Guide for Beginners](https://www.google.com/search?q=https://wiki.ubuntu.com/LVM).