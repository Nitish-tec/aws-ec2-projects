# AWS EC2 Projects

## Project 1: Launch EC2 Instance

### Steps
1. Login to AWS Console
2. Go to EC2 Dashboard
3. Click Launch Instance
4. Select Amazon Linux 2
5. Choose t2.micro
6. Create Key Pair
7. Configure Security Group
8. Allow SSH (22)
9. Launch Instance

---

## Project 2: Connect EC2 Using SSH

```bash
ssh -i key.pem ec2-user@public-ip
```

---

## Project 3: Attach EBS Volume

### Steps
1. Create EBS Volume
2. Attach Volume to EC2
3. Check Disk

```bash
lsblk
```

### Format Disk

```bash
sudo mkfs.xfs /dev/xvdf
```

### Mount Disk

```bash
sudo mount /dev/xvdf /mnt
```

### Verify

```bash
df -h
```

---

## Project 4: Apache Web Server Setup

### Install Apache

```bash
sudo yum install httpd -y
```

### Start Apache

```bash
sudo systemctl start httpd
sudo systemctl enable httpd
```

### Check Status

```bash
sudo systemctl status httpd
```

### Create Test Page

```bash
echo "Welcome to AWS EC2" | sudo tee /var/www/html/index.html
```

---

## Project 5: Security Group Configuration

### Allowed Ports

- SSH : 22
- HTTP : 80
- HTTPS : 443

---

## AWS Services Used

- EC2
- EBS
- Security Groups
- Key Pairs
- VPC

## Author

Nitish Kumar
Linux System Administrator | AWS Cloud Enthusiast | RHCSA Certified
