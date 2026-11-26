# Getting-Started-with-Amazon-Linux-Command-Line-Basics-and-Python-Deployment
A hands-on project documenting Linux command line basics, package management (dnf/yum), and installing and running Python programs on Amazon Linux (AWS EC2). Each task includes the commands used, an explanation in my own words, and screenshots as proof of work.

## 📋 Tasks Covered

### Task 1: Launching an Amazon Linux EC2 Instance
Created a virtual server on AWS using the EC2 service and connected to it remotely. This is the base environment used for all the other tasks.

**Steps:**
1. Logged in to the AWS Management Console and opened the **EC2** dashboard
2. Clicked **Launch Instance** and gave the instance a name
3. Selected **Amazon Linux** as the AMI (operating system image)
4. Chose the **t2.micro / t3.micro** instance type (free tier eligible)
5. Created a new **key pair** (`.pem` file) for secure login
6. Configured the **security group** to allow SSH (port 22)
7. Launched the instance and waited for it to reach the **Running** state
8. Connected to it using **EC2 Instance Connect** (or SSH with the `.pem` key)

> 📸 Screenshots: EC2 dashboard, instance configuration, running instance, successful connection

---

### Task 2: Basic Linux Command Line
Practiced the everyday commands used to move around and manage files on a Linux server.

**Commands practiced:**
| Command | Purpose |
|---|---|
| `pwd` | Show the current directory |
| `ls`, `ls -l` | List files and folders (with permissions) |
| `cd` | Change directory |
| `mkdir` | Create a directory |
| `touch` | Create an empty file |
| `cat` / `nano` | View and edit file contents |
| `cp`, `mv` | Copy and move/rename files |
| `rm` | Delete files and folders |
| `whoami`, `uname -a` | Check the current user and system info |
| `df -h`, `free -h` | Check disk and memory usage |

> 📸 Screenshots: commands and their output

---

### Task 3: Package Management with dnf / yum
Learned how Amazon Linux installs, updates, and removes software using its package manager.

**Steps:**
1. Updated the system packages: `sudo dnf update -y`
2. Searched for a package: `dnf search <package>`
3. Installed a package: `sudo dnf install <package> -y`
4. Checked installed packages: `dnf list installed`
5. Removed a package: `sudo dnf remove <package> -y`

> 📸 Screenshots: update, installation, and verification output

---

### Task 4: Installing Python and Running a Program
Installed Python on the EC2 instance, wrote a simple program, and executed it on the server.

**Steps:**
1. Checked whether Python was already installed: `python3 --version`
2. Installed it if needed: `sudo dnf install python3 -y`
3. Created a script: `nano hello.py`
4. Wrote a basic program, for example `print("Hello from Amazon Linux!")`
5. Ran the program: `python3 hello.py`
6. Verified the output in the terminal

> 📸 Screenshots: Python version, script code, program output

---

## 🧠 What I Learned
- How to launch and connect to a cloud server on AWS EC2
- How the Linux file system and basic commands work
- How package management works on Amazon Linux
- How to run code on a remote server instead of a local machine
- The importance of security groups and key pairs for server access

## ⚠️ Cleanup
Stopped/terminated the EC2 instance after finishing to avoid unexpected AWS charges.
