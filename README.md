# Creating-an-AMI-on-AWS
Creation of Amazon Machine Images (AMIs) from EC2 instances on AWS.
## Step 1: Launch an EC2 Instance

1. Go to AWS Console → EC2
2. Launch Instance.
    - Name → MY_AMI
    - Choose AMI → Amazon Linux.
    - Instance type → t2.micro
    - Key pair → pem_server_key
    - security group → launch-wizard-1

![Project Screenshot](/images/launch-instance.jpg)

## Step 2: Create the AMI from the EC2 instance

1. Go to EC2 service under instance 
2. choose the instance you want to create the AMI
3. Click on **Action** tab
4. Go to **Image and templates → Create Image**
    - **Image name**: Give a name (e.g., `my-server-image`)
    - **Description**: Optional (this is my server image)
5. Click the **"Create Image"** button

![Project Screenshot](/images/ami-create1.jpg)
![Project Screenshot](/images/ami-create2.jpg)
![Project Screenshot](/images/ami-done.jpg)

## Step 3: Delete an AMI  and Instance

1. Go to AWS Console →  Click on AMIs
2. Select the AMI you wish to delete
3. Go to the Actions menu, choose Deregister AMI.
4. check mark Delete associated snapshots
5. Click on the **Deregister AMI**.
![Project Screenshot](/images/us-ami-delete.jpg)
![Project Screenshot](/images/us-ami-delete2.jpg)
7. Go to EC2 → Select instance you want to delete instance 
8. Go to Instance State
9. **Terminate (delete) instance**
![Project Screenshot](/images/instance-delete.jpg)
![Project Screenshot](/images/instance-delete2.jpg)
