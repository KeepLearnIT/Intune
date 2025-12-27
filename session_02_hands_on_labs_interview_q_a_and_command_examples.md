# Section 2: Linux Server Fundamentals & Secure Access Basics 

#hands_on_labs_interview_q_a_and_command_examples.

---

## 1️⃣ Linux Commands – With Real Examples & Explanation

### 🔹 pwd (Present Working Directory)
```
pwd
```
**Output:**
```
/home/ec2-user
```
👉 Shows your current location in the server.

---

### 🔹 ls (List Files)
```
ls
```
Lists files and folders in current directory.

```
ls -l
```
Long format (permissions, owner, size, date).

```
ls -la
```
Includes hidden files (starting with `.`).

---

### 🔹 cd (Change Directory)
```
cd devops
```
Move into devops directory.

```
cd ..
```
Move one level back.

```
cd /
```
Go to root directory.

---

### 🔹 touch (Create File)
```
touch devops.txt
```
Creates an empty file.

---

### 🔹 cat (Read / Write File)
```
cat devops.txt
```
Read file content.

```
cat > devops.txt
```
Write content (overwrite).

```
cat >> devops.txt
```
Append content.

---

### 🔹 mkdir & rm
```
mkdir aws
rm devops.txt
rm -r aws
```
Create and delete files/folders.

---

## 2️⃣ Session-02 Interview Questions & Answers

### Q1. What is DevOps?
**DevOps is a culture that combines development and operations to deliver software faster and reliably.**

---

### Q2. Difference between Waterfall, Agile, and DevOps?
- Waterfall → One-time delivery
- Agile → Incremental development
- DevOps → Continuous development + deployment

---

### Q3. Why Linux is preferred for servers?
- Free & open-source
- Less resource usage
- High security
- Easy automation

---

### Q4. What is SSH?
**SSH is a secure protocol used to connect to Linux servers remotely.**

---

### Q5. What is a Security Group?
**A security group is a virtual firewall that controls inbound and outbound traffic.**

---

### Q6. What is key-based authentication?
**Authentication using public and private key pairs instead of passwords.**

---

### Q7. Difference between public key and private key?
- Public key → Stored on server
- Private key → Stored with user

---

### Q8. What is a port?
**A port is a logical door through which services communicate.**

---

### Q9. What does 0.0.0.0/0 mean?
**It allows traffic from anywhere on the internet.**

---

### Q10. What is CRUD?
**CRUD stands for Create, Read, Update, Delete.**

---

## 3️⃣ Hands-on Lab – Practice Checklist (Session-02)

### 🔹 Lab 1: AWS EC2 Creation
- Create AWS account
- Login to AWS Console
- Go to EC2
- Launch instance
- Choose Amazon Linux 2023
- Select t2.micro

---

### 🔹 Lab 2: Key Pair & Security Group
- Create key pair (.pem)
- Create security group
- Allow SSH (22)
- Source: Your IP / 0.0.0.0/0

---

### 🔹 Lab 3: Connect to Server

```
ssh -i devops.pem ec2-user@<public-ip>
```

Expected result:
```
[ec2-user@ip-xx-xx-xx ~]$
```

---

### 🔹 Lab 4: Linux Practice

```
pwd
ls
mkdir devops
cd devops
touch notes.txt
cat > notes.txt
ls -la
```

---

### 🔹 Lab 5: File Operations

```
cat notes.txt
mv notes.txt linux.txt
rm linux.txt
```

---

## 4️⃣ Common Errors & Fixes

### ❌ Permission denied
✅ Check key permissions:
```
chmod 400 devops.pem
```

---

### ❌ Connection timeout
✅ Check:
- Security group
- Port 22 allowed
- Correct IP

---

## 5️⃣ Session-02 Final Summary

- Linux is the backbone of DevOps
- SSH is the gateway to servers
- Commands control everything
- Practice daily to gain confidence

---

🎯 **Next Session Ready Topics**
- Git & GitHub
- CI/CD basics
- Jenkins introduction
- Docker fundamentals

