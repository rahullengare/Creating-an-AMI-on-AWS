# Creating-an-AMI-on-AWS
Creation of Amazon Machine Images (AMIs) from EC2 instances on AWS.
### 📌 About Project

- This project focuses on **creating a custom Amazon Machine Image (AMI)** on AWS.
- An AMI is a **pre-configured template** containing an operating system, application server, and applications, used to launch EC2 instances quickly.
- The main goal is to **capture a configured EC2 instance** and convert it into a reusable image for scalability and reliability.

---

### 🛠️ Technology Used

1. **Amazon Web Services (AWS)** – Cloud platform for hosting and managing infrastructure.
2. **EC2 (Elastic Compute Cloud)** – Virtual server instances used to configure the environment before creating an AMI.
3. **Amazon Machine Image (AMI)** – Template that stores the instance configuration.
4. **AWS Management Console / AWS CLI** – Tools for creating and managing AMIs.

---

### What is AMI?

- **AMI (Amazon Machine Image):** An **Amazon Machine Image (AMI)** is a pre-configured template in AWS that contains an operating system, application server, and required software, which acts as a blueprint to launch EC2 instances, enabling easy scaling, backup, and rapid deployment of identical virtual servers in the cloud.

### What is EC2?

- **EC2 Instance:** An **EC2 instance (Elastic Compute Cloud instance)** is a virtual server in Amazon Web Services (AWS) used to run applications on the cloud, providing resizable compute capacity where you can install operating systems, deploy software, and host workloads, making it similar to a computer in the cloud that can be scaled up or down based on your needs.

---
## Step 1: Launch an EC2 Instance

1. Go to AWS Console → EC2
2. Launch Instance.
    - Name → MY_AMI
    - Choose AMI → Amazon Linux.
    - Instance type → t2.micro
    - Key pair → pem_server_key
    - security group → launch-wizard-1

![Project Screenshot](/images/launch-instance.png)

## Step 2: Create the AMI from the EC2 instance

1. Go to EC2 service under instance 
2. choose the instance you want to create the AMI
3. Click on **Action** tab
4. Go to **Image and templates → Create Image**
    - **Image name**: Give a name (e.g., `my-server-image`)
    - **Description**: Optional (this is my server image)
5. Click the **"Create Image"** button

![Project Screenshot](/images/ami-create1.png)
![Project Screenshot](/images/ami-create2.png)
![Project Screenshot](/images/ami-done.png)

## Step 3: Delete an AMI  and Instance

1. Go to AWS Console →  Click on AMIs
2. Select the AMI you wish to delete
3. Go to the Actions menu, choose Deregister AMI.
4. check mark Delete associated snapshots
5. Click on the **Deregister AMI**.
![Project Screenshot](/images/us-ami-delete.png)
![Project Screenshot](/images/us-ami-delete2.png)
7. Go to EC2 → Select instance you want to delete instance 
8. Go to Instance State
9. **Terminate (delete) instance**
![Project Screenshot](/images/instance-delete.png)
![Project Screenshot](/images/instance-delete2.png)

