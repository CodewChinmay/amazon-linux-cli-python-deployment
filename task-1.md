# Task 1: Launching an Amazon Linux EC2 Instance

Created a virtual server on AWS using the EC2 service and connected to it remotely. This is the base environment used for all the other tasks.

## Steps
1. Logged in to the AWS Management Console and opened the **EC2** dashboard
2. Clicked **Launch Instance** and gave the instance a name
3. Selected **Amazon Linux** as the AMI (operating system image)
4. Chose the **t2.micro / t3.micro** instance type (free tier eligible)
5. Created a new **key pair** (`.pem` file) for secure login
6. Configured the **security group** to allow SSH (port 22)
7. Launched the instance and waited for it to reach the **Running** state
8. Connected to it using **EC2 Instance Connect** (or SSH with the `.pem` key)

## 📸 Screenshots
EC2 dashboard, instance configuration, running instance, successful connection

---
[⬅ Back to main page](../README.md) | [Next: Task 2 ➡](task-2-linux-command-line.md)
