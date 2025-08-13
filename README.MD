# Lab: Launching an AWS EC2 Windows Server 2022 Instance

**Instructor**: George Ensminger  
**Objective**: Launch and connect to an AWS EC2 instance running **Windows Server 2022**, utilizing the Free Tier where applicable.

---

## Prerequisites

- An active AWS account, ideally Free Tier eligible  
- Familiarity with AWS Management Console basics  
- A Remote Desktop (RDP) client installed on your local machine

---

## Step-by-Step Instructions

### 1. Log in & Open EC2 Dashboard
1. Sign in to the [AWS Management Console](https://console.aws.amazon.com/) and ensure you’re in your preferred AWS Region (e.g., `us-east-1`) :contentReference[oaicite:0]{index=0}.  
2. In the services search bar, type **EC2** and open the EC2 Dashboard :contentReference[oaicite:1]{index=1}.

### 2. Launch a Windows Server 2022 Instance
1. Click **Launch Instance**.  
2. In **Name and tags**, assign a meaningful name (e.g., `Demo-ec2-instance-Lab`).  
3. Under **Amazon Machine Image (AMI)**, select **Microsoft Windows Server 2022 Base**.  
4. For **Instance Type**, choose **t2.micro** (Free Tier eligible).  
5. Move to the **Key Pair** section: create a new key pair (e.g., `EC2-Demo-Key2.pem`), download the `.pem` file, and store it securely.  
6. In **Network & Security** or **Security group**, ensure RDP (port 3389) is allowed. For lab purposes, you may set the source to your IP or `Anywhere (0.0.0.0/0)` but note this is **not** recommended for production environments.  
7. Keep **Storage** set to default (e.g., 30 GiB, gp2).  
8. Review all settings and click **Launch instance**.

### 3. Monitor Instance Status
- Navigate to **Instances (running)** in the EC2 console.  
- Wait until its status shows **running** with **2/2 checks passed**.

---

## Lab Summary Table

| Step | Action |
|------|--------|
| 1 | Log in and open EC2 Dashboard |
| 2 | Launch a Windows Server 2022 instance: name, AMI, t2.micro, key pair, security group |
| 3 | Wait for instance status **running** and **2/2 checks passed** |


---

## Tips & Best Practices

- **Naming & Tagging**: Use clear names/tags for resource management.  
- **Security**: For RDP access, restrict to your IP rather than opening to all.  
- **Key Pair Safety**: Keep the `.pem` file private.  
- **Automation**: Explore **EC2Launch v2** configuration for automated tasks.

---
