# Introduction to Virtualization and Cloud Computing

## Topics Covered

### 1. **Introduction to Virtualization**
- **What is Virtualization?**
  - Virtualization is the creation of a virtual version of hardware, allowing multiple operating systems to run on a single physical machine.
  
- **Types of Virtualization**
  - Server Virtualization: Multiple virtual servers on one physical machine.
  - Storage Virtualization: Combining multiple physical storage devices into a single virtual unit.
  - Network Virtualization: Abstracting network resources into a manageable virtual framework.

- **Key Benefits**:
  - Efficient resource utilization
  - Cost savings
  - Scalability
  - Simplified management

#### **Deep Dive Knowledge**:
- Virtualization uses a hypervisor (like VMware or VirtualBox) to manage VMs.
- Popular tools include KVM, Xen, and Microsoft Hyper-V.
- Real-time Example: A company can run a legacy Windows app on a Linux server using virtualization.

#### **Simple Explanation**:
- Think of virtualization as renting rooms in a house (the physical machine) where each room (VM) has its own tenant (OS).

### 2. **Virtualization vs Cloud**
- Virtualization is a foundational technology; cloud computing builds on it.
- **Comparison Table**:
  | **Feature**          | **Virtualization**                     | **Cloud Computing**                       |
  |-----------------------|----------------------------------------|-------------------------------------------|
  | **Definition**        | Technology to create virtual environments. | Delivery of on-demand computing resources via the internet. |
  | **Deployment**        | Local (on-premises servers).           | Hosted on the internet.                   |
  | **Scalability**       | Limited by physical hardware.          | Highly scalable without physical limits.  |
  | **Access**            | Internal network only.                | Accessible from anywhere with an internet connection. |

#### **Deep Dive Knowledge**:
- Virtualization focuses on optimizing hardware usage, while cloud emphasizes service delivery and flexibility.
- Real-time Example: Virtualization is like owning apartments in a building, whereas cloud is like Airbnb where anyone can rent as needed.

### 3. **Cloud Models (IaaS, PaaS, SaaS)**
- **Infrastructure as a Service (IaaS)**:
  - Virtualized hardware resources.
  - **Examples**: AWS EC2, Google Compute Engine.
  - **Real-time Example**: Hosting a website on AWS EC2 where you control the OS and applications.

- **Platform as a Service (PaaS)**:
  - Platforms for application development.
  - **Examples**: AWS Elastic Beanstalk, Google App Engine.
  - **Real-time Example**: Using AWS Elastic Beanstalk to deploy a web app without worrying about the underlying infrastructure.

- **Software as a Service (SaaS)**:
  - Software accessible over the internet.
  - **Examples**: Gmail, Salesforce.
  - **Real-time Example**: Using Google Docs to collaborate on documents in real-time.

#### **Simple Explanation**:
- **IaaS**: Like renting a raw apartment and furnishing it yourself.
- **PaaS**: Like renting a fully furnished apartment but adding your own decorations.
- **SaaS**: Like booking a hotel room where everything is ready.

### 4. **AWS Account Creation**

Follow these steps to create your AWS account:
1. Visit [AWS Free Tier](https://aws.amazon.com/free/).
2. **Sign Up**:
   - Enter your email address and password.
   - Create an account name.
3. **Account Type**: Choose "Personal" or "Professional."
4. **Payment Method**: Add a valid credit/debit card for identity verification.
5. **Verify Identity**: Enter your mobile number for OTP verification.
6. **Select Support Plan**: Choose "Basic (Free)."
7. Log in to the AWS Management Console.

#### **Deep Dive Knowledge**:
- AWS Free Tier offers 12 months of free services like EC2, S3, and Lambda with usage limits.
- Real-time Example: Use the free tier to deploy a simple static website using S3 and monitor costs via the AWS Billing Dashboard.

---

## Hands-On Practice
- **Objective**: Create an AWS account and explore the Management Console.
- **Tasks**:
  1. Sign up for an AWS account using the steps above.
  2. Navigate through the AWS Console to identify key services like EC2, S3, and RDS.

---

## Resources
- [AWS Free Tier Overview](https://aws.amazon.com/free/)
- [AWS Documentation](https://docs.aws.amazon.com/)
- [Virtualization Basics](https://www.vmware.com/topics/glossary/content/virtualization.html)

---

## Key Takeaways
- Virtualization is the backbone of cloud computing.
- Understand the differences between IaaS, PaaS, and SaaS.
- AWS provides a user-friendly interface for cloud services.

----

# Introduction to AWS Dashboard and EC2

## Topics Covered

### 1. **Introduction to AWS Dashboard**
The AWS Management Console is the primary interface for managing AWS resources. It is a web application that allows you to:
- Access and manage services like EC2, S3, RDS, and Lambda.
- Monitor your usage and billing.
- Set up security configurations and permissions.

#### **Key Components of the Dashboard**:
1. **Navigation Bar**: Displays your logged-in account, active region, and access to global services like billing and support.
2. **Service Search Bar**: Helps you quickly locate AWS services by name.
3. **Resource Groups**: Allows grouping and managing related resources.
4. **Recent Services**: A list of services you used recently for quick access.
5. **Build a Solution**: Quick links to common tasks such as launching an instance or creating a database.

#### **Best Practices**:
- Always verify the active region to avoid deploying resources in unintended locations.
- Use the Billing Dashboard to track costs and identify unusual usage patterns.

---

### 2. **Region vs Availability Zone (AZ)**
AWS resources are deployed in Regions and Availability Zones to ensure high availability, fault tolerance, and low latency.

#### **Region**:
- A geographical location, such as **US East (N. Virginia)** or **Asia Pacific (Mumbai)**.
- Each region is independent and contains multiple Availability Zones.
- Choose a region based on proximity to your users, compliance requirements, and cost considerations.

#### **Availability Zone (AZ)**:
- A physically distinct data center within a region.
- Each AZ is isolated but connected to other AZs in the same region via low-latency links.
- Example: The **Asia Pacific (Mumbai)** region has three AZs: ap-south-1a, ap-south-1b, and ap-south-1c.

#### **Why Regions and AZs Matter**:
- **High Availability**: Deploy resources across multiple AZs to ensure uptime during failures.
- **Low Latency**: Choose regions close to your users to minimize network delays.
- **Cost Optimization**: Some regions have lower costs for the same services.

---

### 3. **Introduction to EC2 Service**
Amazon Elastic Compute Cloud (EC2) is a core service for deploying scalable virtual servers in the cloud.

#### **Features**:
- **Scalability**: Easily scale instances up or down based on demand.
- **Customizable Instances**: Choose instance types based on CPU, memory, and storage needs.
- **Secure Access**: Use SSH keys and security groups for secure connections.
- **Flexible Pricing**:
  - **On-Demand Instances**: Pay per hour with no long-term commitments.
  - **Reserved Instances**: Commit for 1-3 years for lower prices.
  - **Spot Instances**: Bid for unused capacity at discounted rates.

#### **Use Cases**:
- Hosting web applications.
- Running batch jobs or machine learning models.
- Building development and testing environments.

---

### 4. **Creating Your First EC2 Instance (Ubuntu)**

#### **Steps to Launch an EC2 Instance**:
1. **Navigate to EC2 Service**:
   - Log in to the AWS Management Console.
   - Search for "EC2" in the service search bar and select it.

2. **Launch Instance**:
   - Click on the "Launch Instance" button.

3. **Choose an Amazon Machine Image (AMI)**:
   - Select **Ubuntu Server 20.04 LTS** (or another version as needed).

4. **Select Instance Type**:
   - Choose **t2.micro** for free tier eligibility (1 vCPU, 1 GB RAM).

5. **Configure Instance Details**:
   - Leave the default settings.
   - Optionally, enable Auto-Assign Public IP for internet access.

6. **Add Storage**:
   - Keep the default storage size (e.g., 8 GB).
   - Modify if additional storage is required.

7. **Add Tags**:
   - Create a tag to identify your instance (e.g., `Key: Name, Value: MyFirstInstance`).

8. **Configure Security Group**:
   - Create a new security group.
   - Add an inbound rule to allow **SSH (port 22)** from your IP address.

9. **Review and Launch**:
   - Verify your settings and click "Launch."
   - Select an existing key pair or create a new one for SSH access.

10. **Access Your Instance**:
    - Download the private key file (`.pem`) if creating a new key pair.
    - Use an SSH client (like PuTTY or Terminal) to connect:
      ```bash
      ssh -i /path/to/key.pem ubuntu@<Public-IP-Address>
      ```

#### **Best Practices**:
- Always restrict SSH access to specific IP addresses for security.
- Use Elastic IPs for instances requiring a static public IP.

---

## Resources
- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [AWS Free Tier Details](https://aws.amazon.com/free/)
- [SSH Key Management](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html)

---

## Key Takeaways
- The AWS Dashboard is your central hub for managing cloud resources.
- Regions and AZs provide resilience and flexibility for deployments.
- EC2 is a powerful service for launching virtual servers with customizable configurations.

----

# Security Groups and Instance Management

## Topics Covered

### 1. **Security Group (SSH and RDP Port)**
Security Groups act as virtual firewalls that control inbound and outbound traffic for your AWS instances. 

#### **Key Concepts**:
- **Inbound Rules**: Define the traffic allowed to reach your instance.
- **Outbound Rules**: Define the traffic allowed to leave your instance.
- Rules specify:
  - Protocol (e.g., TCP, UDP, ICMP).
  - Port Range (e.g., 22 for SSH, 3389 for RDP).
  - Source (IP address or another security group).

#### **Common Ports**:
- **SSH (Port 22)**: Used for secure remote access to Linux instances.
- **RDP (Port 3389)**: Used for remote access to Windows instances.

#### **Best Practices**:
- Restrict access to specific IP ranges for security.
- Use custom security groups for different applications or roles.

#### **Steps to Configure a Security Group**:
1. Open the EC2 Dashboard and navigate to "Security Groups."
2. Create a new security group.
3. Add inbound rules:
   - For SSH: Protocol = TCP, Port = 22, Source = My IP.
   - For RDP: Protocol = TCP, Port = 3389, Source = My IP.
4. Add outbound rules (default allows all traffic).
5. Attach the security group to your instance during or after creation.

---
# SSH Service: Secure Shell Basics

## What is SSH?
SSH (Secure Shell) is a cryptographic network protocol that provides a secure way to access remote servers and systems. It allows administrators and developers to log in, execute commands, and manage resources over an encrypted connection.

---

## Key Features of SSH
- **Secure Communication**: Uses encryption to secure the connection.
- **Authentication**: Supports various methods like password-based or key-based authentication.
- **Port Forwarding**: Allows secure tunneling of other protocols.
- **File Transfers**: Includes tools like `scp` and `rsync` for transferring files securely.
- **Session Management**: Offers features like persistent sessions and command execution.

---

## SSH in AWS
SSH is commonly used in AWS to manage EC2 instances and other Linux-based resources securely.

### Default Settings for AWS EC2:
- **Port**: 22 (must be open in the security group).
- **Authentication**: Key-pair (`.pem` file) generated during instance creation.

---

## Setting Up SSH for Remote Access

### 1. **Installing SSH Client**
Most operating systems come with SSH clients pre-installed. For example:
- **Linux/MacOS**: SSH is available by default in the terminal.
- **Windows**: Use `ssh` in PowerShell or install third-party tools like PuTTY.

### 2. **Connect to a Remote Server**
To connect to a remote server:
```bash
ssh -i /path/to/key.pem username@<remote-ip-address>
```
- Replace `/path/to/key.pem` with the path to your private key file.
- Replace `username` with the server's default user (e.g., `ubuntu` for Ubuntu instances).
- Replace `<remote-ip-address>` with the public IP of the remote server.

---

### 3. **Configuring SSH Access on AWS EC2**
1. **Verify Security Group**:
   - Ensure the inbound rule allows SSH (port 22).
   - Restrict access to your IP address for enhanced security.

2. **Set File Permissions**:
   ```bash
   chmod 400 /path/to/key.pem
   ```
   This ensures that the private key has the correct permissions.

3. **Connect Using the SSH Command**:
   ```bash
   ssh -i /path/to/key.pem ubuntu@<Public-IP>
   ```

4. **Troubleshooting Connection Issues**:
   - Verify that the instance is running.
   - Check the public IP and ensure it matches the instance.
   - Ensure your IP is allowed in the security group.

---

## Resources
- [Official OpenSSH Documentation](https://www.openssh.com/manual.html)
- [AWS EC2 Key Pair Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html)
- [Secure File Transfer with scp](https://linux.die.net/man/1/scp)

---

## Summary
SSH is an essential tool for securely managing remote servers. By understanding its features and applying best practices, you can ensure secure and efficient access to your resources. Let’s practice setting up and using SSH in our next session! 🚀


---
### 2. **Create Instance of Windows**
AWS EC2 supports launching instances with Windows operating systems for various use cases, such as hosting .NET applications or running Windows-based tools.

#### **Steps to Launch a Windows Instance**:
1. **Navigate to EC2**:
   - Log in to the AWS Management Console.
   - Search for "EC2" and open the service.

2. **Launch Instance**:
   - Click on "Launch Instance."

3. **Choose AMI**:
   - Select a Windows Server AMI, such as **Windows Server 2019 Base**.

4. **Choose Instance Type**:
   - Select **t2.micro** (free tier eligible).

5. **Configure Instance Details**:
   - Leave default settings.
   - Optionally, assign an Elastic IP for a static public IP.

6. **Add Storage**:
   - Keep the default storage size or increase based on your needs.

7. **Configure Security Group**:
   - Add an inbound rule for RDP (port 3389).

8. **Launch and Download Key Pair**:
   - Download the `.pem` key file for accessing the instance.

9. **Retrieve Password**:
   - After launching, go to the instance details.
   - Click on "Get Windows Password" and decrypt it using the `.pem` key file.

10. **Connect to the Instance**:
    - Use Remote Desktop Protocol (RDP) on your local machine:
      - Hostname: Public IP of the instance.
      - Username: Administrator.
      - Password: Retrieved from the AWS console.

---

### 3. **Remote Access of Linux and Windows Machines**

#### **Linux Instance Remote Access**:
1. **Prerequisites**:
   - Ensure SSH is allowed in the security group.
   - Have the `.pem` key file downloaded during instance creation.

2. **Using SSH Command**:
   ```bash
   ssh -i /path/to/key.pem ubuntu@<Public-IP>
   ```

3. **Troubleshooting**:
   - Verify that the instance is running.
   - Ensure your local machine's IP is added to the security group.

#### **Windows Instance Remote Access**:
1. **Enable RDP Access**:
   - Ensure RDP is allowed in the security group.

2. **Using Remote Desktop Client**:
   - Open Remote Desktop Connection (Windows) or install an RDP client (Linux/Mac).
   - Enter the public IP address of the instance.
   - Use the Administrator username and decrypted password.

3. **Troubleshooting**:
   - Check the RDP port in the security group.
   - Ensure the instance has a public IP.

---

## Resources
- [AWS Security Group Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html)
- [Launching Windows Instances](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/LaunchingAndUsingInstances.html)
- [Connecting to Linux Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html)

---

## Key Takeaways
- Security Groups are essential for controlling access to your instances.
- RDP and SSH are the primary protocols for remote access to Windows and Linux instances, respectively.
- Proper configuration of Security Groups ensures both accessibility and security.


----
# 


## 1. **Deploy Web Server Using NGINX**
NGINX is a lightweight, high-performance web server and reverse proxy server used to host websites and applications.

### **Steps to Deploy NGINX**:
1. **Update the Package Manager**:
   ```bash
   sudo apt update
   ```

2. **Install NGINX**:
   ```bash
   sudo apt install nginx -y
   ```

3. **Start and Enable the NGINX Service**:
   ```bash
   sudo systemctl start nginx
   sudo systemctl enable nginx
   ```

4. **Verify the Installation**:
   - Open a web browser and navigate to the server's public IP.
   - You should see the default NGINX welcome page.

5. **Configure the Firewall** (If Enabled):
   - Allow HTTP and HTTPS traffic:
     ```bash
     sudo ufw allow 'Nginx Full'
     ```
   - Check the firewall status:
     ```bash
     sudo ufw status
     ```

6. **Host a Custom Website**:
   - Replace the default content:
     ```bash
     sudo nano /var/www/html/index.html
     ```
     Add your HTML content and save the file.

7. **Restart NGINX**:
   ```bash
   sudo systemctl restart nginx
   ```

8. **Verify the Website**:
   - Open the server's public IP in a web browser to view your hosted site.

---

## 2. **Deploy Web Server Using HTTPD**
HTTPD (Apache HTTP Server) is a widely-used open-source web server known for its flexibility and robustness.

### **Steps to Deploy HTTPD**:
1. **Update the Package Manager**:
   ```bash
   sudo yum update -y
   ```

2. **Install HTTPD**:
   ```bash
   sudo yum install httpd -y
   ```

3. **Start and Enable the HTTPD Service**:
   ```bash
   sudo systemctl start httpd
   sudo systemctl enable httpd
   ```

4. **Verify the Installation**:
   - Open a web browser and navigate to the server's public IP.
   - You should see the default Apache HTTPD test page.

5. **Configure the Firewall**:
   - Allow HTTP and HTTPS traffic:
     ```bash
     sudo firewall-cmd --permanent --add-service=http
     sudo firewall-cmd --permanent --add-service=https
     sudo firewall-cmd --reload
     ```

6. **Host a Custom Website**:
   - Navigate to the default document root:
     ```bash
     cd /var/www/html
     ```
   - Replace or add content to `index.html`:
     ```bash
     sudo nano index.html
     ```
     Add your HTML content and save the file.

7. **Restart HTTPD**:
   ```bash
   sudo systemctl restart httpd
   ```

8. **Verify the Website**:
   - Open the server's public IP in a web browser to view your hosted site.

---

## Resources
- [NGINX Documentation](https://nginx.org/en/docs/)
- [Apache HTTPD Documentation](https://httpd.apache.org/docs/)
- [OpenSSH Documentation](https://www.openssh.com/manual.html)
- [Linux User Management Guide](https://linuxize.com/post/how-to-create-a-new-user-on-linux/)

---

## Key Takeaways
- NGINX and HTTPD provide robust platforms for hosting web applications.

------------

# Amazon EC2: Comprehensive Guide

This README provides detailed information about Amazon EC2, covering its dashboard, instance types, status checks, AMIs, launch templates, and purchasing options. The content is organized to ensure clarity and practical usability for users.

---

## **Amazon EC2 Dashboard Overview**

The Amazon EC2 Dashboard provides a centralized interface to manage EC2 resources. Key components of the dashboard include:

- **Instances**: View and manage running instances.
- **Launch Instances**: Create new EC2 instances using preconfigured settings.
- **Instance Types**: Explore the various types of instances available.
- **Elastic Block Store (EBS)**: Manage attached storage volumes.
- **Key Pairs**: Secure access to instances with SSH keys.
- **Security Groups**: Configure firewall settings for your instances.
- **Elastic IPs**: Allocate static public IP addresses to your instances.

---

## **Instance Types**

Amazon EC2 offers a wide range of instance types to suit diverse workloads. Below are the main categories:

### **General Purpose**
Balanced compute, memory, and storage.
- Examples: M5, T2, T3, M6a, Mac2

### **Compute Optimized**
Ideal for compute-intensive tasks.
- Examples: C5, C6i, C7g

### **Memory Optimized**
Designed for high-performance databases and memory-intensive applications.
- Examples: R5, X1, X2idn

### **Storage Optimized**
For workloads requiring high, sequential read/write access to large data sets.
- Examples: I3, D2, H1

### **Accelerated Computing**
Designed for applications requiring GPUs or hardware accelerators.
- Examples: P3, G5, Inf1

### **High-Performance Computing (HPC)**
For HPC applications requiring low latency and high performance.
- Examples: Hpc6a, Hpc7g

[Refer to AWS Instance Types Documentation](https://aws.amazon.com/ec2/instance-types/)

---

## **Status Checks for Amazon EC2 Instances**

### **Overview**
Amazon EC2 continuously monitors instance health via automated status checks. These checks ensure instances are running without issues.

- **System Status Check**: Verifies the infrastructure hosting your instance is functioning correctly.
- **Instance Status Check**: Monitors the software and network configuration of your instance.

### **Common Failure Causes**
- Networking issues
- Exhausted memory
- Corrupted file systems
- Kernel incompatibilities

### **CloudWatch Alarms**
You can set alarms to monitor status checks and take automated actions, such as instance recovery, if issues are detected.

[Refer to AWS Status Checks Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/monitoring-system-instance-status-check.html)

---

## **AMI (Amazon Machine Image)**

### **AMI Types**
1. **EBS-backed AMI**: Boot volume stored on Amazon EBS.
2. **Instance-store-backed AMI**: Boot volume stored on local instance storage.

### **Creating an AMI**
1. Navigate to the EC2 dashboard.
2. Select the instance you wish to create an AMI from.
3. Choose **Actions > Image > Create Image**.
4. Provide the necessary details and click **Create Image**.

### **Copying an AMI**
You can copy AMIs between regions to enhance redundancy or deploy in multiple regions.

[Refer to AWS AMI Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)

---

## **Launch Templates**

Launch templates enable consistent configuration of EC2 instances. They support settings like:
- AMI ID
- Instance Type
- Security Groups
- Key Pair

### **Creating a Launch Template**
1. Open the EC2 dashboard.
2. Navigate to **Launch Templates**.
3. Click **Create Launch Template**.
4. Fill in required details, including AMI ID, instance type, and security groups.

[Refer to AWS Launch Template Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html)

---

# Purchasing Options

**On-Demand** - 
- Pay for what you use
- Linux or Windows - billing per second after the first minute
- All other OS - billing per hour
- It has the highest cost but no upfront payment
- No long-term commitment
- Recommended for short term and un-interrupted workloads where you can't predict the how application will behave 
- ideal for auto-scaling and unpredictable workloads

**Reserved Instances** - 
- Up to 72% discount compared to on-demand
- You reserve specific instance attributes (instance type, region, tenancy, os)
- Reservation period - 1 year(+discount) or 3 years(+++discount)
- Payment option - No upfront(+), partial upfront(++), all upfront(+++)
- Reserved Instances Scope - Regional or Zonal 
- Recommended for steady-state usage applications (eg. database)
- You can buy or sell in the reserved instance marketplace 
- Convertible Reserved Instance  - Can change the instance type, instance family, OS, scope, and tenancy. Up to 66% discount

**Spot Instances** - 
- Can get discounts up to 90% compared to on demand
- Instances that you can "lose" at any point of time if your max price is less that current spot price
- The most cost-efficient instances in AWS
- Useful for workloads that are resilient to failure - batch jobs, data analysis, image processing, any distributed workloads, workloads with a flexible start and end time
- not suitable for critical jobs or databases

**Dedicated Hosts** - 
- Physical servers dedicated just for your use
- You then have control over which instances are deployed on that host
- Available as on-demand or with a dedicated hosts reservation
- Useful if you have server-bound software licenses that use metrics like per-core, per-socket, per-VM
- Each dedicated host can run only on instance size and type
- Good for regulatory compliance or licensing requiremnets
- Predictable performance
- Complete isolation
- Most expensive option
- Billing is per host

**Dedicated Instances** - 
- Virtualized instances on hardware just for you
- Also uses physically dedicated EC2 servers
- Does not provide additional visibility and controls of dedicated host 
- Billing is per instance 
- May share hardware with other non-dedicated instances in the same account
- Available as on-demand, reserved instances, spot instances
- Cost additional $2 per hour per region

**Capacity Reservations** - 
- Reserve on-demand instances capacity in a specific AZ for any duration 
- You always have access to EC2 capacity when you need it 
- No time commitment (create/cancel anytime), no billing discount
- Combine with regional reserved instances and saving plans to benefit from billing discount
- You are charged at on-demand rate whether you run instances or not
- Suitable for short-term, uninterrupted workloads that need to be in a specific AZ

###**How to choose a purchasing option ???** - 

Let's understand these concepts of purchasing options by taking the example of booking a resort

- **On-demand** - coming and staying in a resort whenever we like, we pay the full price
- **Reserved instances** - like planning ahead and if we plan to stay for a long time, we may get a good discount
- **Spot instances** - the hotel allows people to bid for the empty room and the highest bidder keeps the rooms but can get kicked out anytime if anyone gives high price than them
- **Dedicated hosts** - we book an entire building of the resort 
- **Capacity reservations** - you book a room for a period with full price even if you don't stay


### **Overview**
Amazon EC2 offers several purchasing options to optimize costs:

1. **On-Demand Instances**: Pay for instances by the second.
2. **Savings Plans**: Commit to a consistent usage level for 1 or 3 years.
3. **Reserved Instances**: Commit to specific configurations for 1 or 3 years.
4. **Spot Instances**: Use spare EC2 capacity at reduced costs.
5. **Dedicated Hosts**: Full physical servers for your instances.
6. **Dedicated Instances**: Single-tenant instances.
7. **Capacity Reservations**: Reserve capacity in specific AZs.


---
## **EBS Volumes and Its Types**

Amazon Elastic Block Store (EBS) provides persistent block storage for use with Amazon EC2 instances. These volumes are highly available, reliable, and scalable.

### **Types of EBS Volumes**

1. **General Purpose SSD (gp3, gp2)**
   - Ideal for a wide range of workloads, including boot volumes, dev/test environments, and low-latency interactive apps.
   - **gp3** offers predictable IOPS and lower costs compared to **gp2**.

2. **Provisioned IOPS SSD (io1, io2)**
   - Designed for I/O-intensive applications, such as databases.
   - Offers high durability and supports features like Multi-Attach.

3. **Throughput Optimized HDD (st1)**
   - Suitable for frequently accessed, throughput-intensive workloads such as big data and log processing.

4. **Cold HDD (sc1)**
   - Ideal for infrequently accessed workloads, such as backups and archiving.

5. **Magnetic (Standard)**
   - Suitable for workloads where data is infrequently accessed.

[Refer to AWS EBS Volume Types Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html)

---

## **Attach Volumes, Create Partition, and Mount**

### **Attaching an EBS Volume to an EC2 Instance**
1. Go to the **EC2 Dashboard** on the AWS Management Console.
2. Select **Volumes** from the left menu.
3. Choose the volume you want to attach and click **Actions > Attach Volume**.
4. Select the instance to attach the volume to and click **Attach**.

### **Creating a Partition**
1. SSH into the EC2 instance to which the volume was attached.
2. Use the `lsblk` command to list all block devices and confirm the new volume is attached (e.g., `/dev/xvdf`).
3. Create a partition on the volume using the `fdisk` command:
   ```bash
   sudo fdisk /dev/xvdf
   ```
   - Press `n` to create a new partition.
   - Follow the prompts and press `w` to write changes.
4. Format the partition:
   ```bash
   sudo mkfs.ext4 /dev/xvdf1
   ```

### **Mounting the Volume**
1. Create a mount directory:
   ```bash
   sudo mkdir /mnt/ebs-volume
   ```
2. Mount the volume:
   ```bash
   sudo mount /dev/xvdf1 /mnt/ebs-volume
   ```
3. Verify the volume is mounted:
   ```bash
   df -h
   ```

### **Persisting the Mount (Optional)**
To make the mount persistent across reboots:
1. Open the `/etc/fstab` file:
   ```bash
   sudo nano /etc/fstab
   ```
2. Add the following entry:
   ```bash
   /dev/xvdf1   /mnt/ebs-volume   ext4   defaults,nofail   0   2
   ```
3. Save the file and exit.
4. Test the configuration:
   ```bash
   sudo mount -a
   ```

---

## **Summary**

- **EBS Volumes**: Provide persistent, reliable block storage.
- **Volume Types**: Include SSDs (gp3, gp2, io1, io2), HDDs (st1, sc1), and magnetic storage.
- **Operations**: Attach a volume, create partitions, format, and mount it to an EC2 instance.

----
## **Taking Backup Using Snapshots**

### **Manual Snapshot Creation**
1. Navigate to the **EC2 Dashboard** on the AWS Management Console.
2. Select **Volumes** from the left-hand menu.
3. Choose the volume to back up and click **Actions > Create Snapshot**.
4. Provide a description for the snapshot and click **Create Snapshot**.
5. To view snapshots, navigate to **Snapshots** in the EC2 Dashboard.


## **Automating Snapshots Using Snapshot Policies**

### **Create a Snapshot Lifecycle Policy**
1. Navigate to the **Amazon Data Lifecycle Manager (DLM)** in the AWS Management Console.
2. Click **Create lifecycle policy**.
3. Select **EBS Snapshot policy**.
4. Configure policy details:
   - Select resource type as **Volume**.
   - Add tags to identify the volumes to be included in the policy (e.g., `Environment:Production`).
5. Define a schedule:
   - Specify the frequency of snapshots (e.g., daily).
   - Define a retention period (e.g., retain snapshots for 7 days).
6. Review and create the policy.


## **Summary**

- **Partition Management**: Create and persist partitions using `fstab`.
- **Snapshots**: Manual and CLI-based snapshot creation.
- **Automation**: Implement lifecycle policies for scheduled backups.

---


# 📌 Introduction to NFS  

## 🔹 What is NFS?  
- **NFS = Network File System**  
- It is a way for computers to **share files over a network**.  
- Think of it like **Google Drive or OneDrive**, but for servers inside a network.  
- With NFS, you can create one storage location and let **multiple computers (clients)** connect and use it as if it were their own local disk.  

---

## 🔹 How does it work?  
- Two main parts:  
  1. **NFS Server** → The machine that has the actual storage and shares it.  
  2. **NFS Clients** → Other machines that connect to the server and access files.  

- Clients mount (attach) the shared folder and can **read/write files** just like a normal folder.  

---

## 🔹 Real-life Example  
- Imagine a company office:  
  - The **NFS Server** is like the office filing cabinet.  
  - Employees (clients) don’t keep their own copies, they just **open the same cabinet drawer** and work on the same files.  
  - If one person updates a document, everyone sees the update instantly.  

---

## 🔹 Key Features of NFS  
1. **Centralized Storage** – Files are stored in one place, not scattered across machines.  
2. **Shared Access** – Multiple servers can access the same data.  
3. **Scalability** – Add more clients without copying files everywhere.  
4. **Transparency** – To the client, it looks like a normal folder/directory.  
5. **Uses TCP/UDP Port 2049** – Default port for NFS communication.  

---

## 🔹 Why do we need NFS?  
- Without NFS: Every server would have its **own local files**, making it difficult to share or sync data.  
- With NFS: All servers point to the **same storage**, making collaboration and scaling easier.  

**Use Cases:**  
- Hosting a website on multiple servers → all servers can use **same images, code, or logs** from NFS.  
- In AWS → **EFS (Elastic File System)** is Amazon’s managed NFS service.  

---

## 🔹 Versions of NFS  
- **NFSv2** – Old version, basic sharing.  
- **NFSv3** – Supports large files, better performance.  
- **NFSv4** – Latest, more secure (supports encryption, ACLs).  
- AWS EFS uses **NFSv4.1** by default.  

---

# 📌 NFS in AWS Context  

### Is NFS Region-specific or AZ-specific?  

- **NFS (general protocol)** → Not tied to region/AZ, depends only on network reachability.  

- **Amazon EFS (managed NFS)**:  
  - **Region-specific** → An EFS file system exists only in one AWS region.  
  - **Multi-AZ** → Data is stored across multiple Availability Zones within that region.  
  - Instances in different AZs of the same region can mount the same EFS file system.  

---

## ✅ Quick Summary  
- **NFS protocol** → Not tied to region/AZ, just needs network connectivity.  
- **AWS EFS** →  
  - Region-specific.  
  - Multi-AZ within that region for high availability.  

👉 In AWS terms:  
**EFS is region-specific, but can be accessed from multiple AZs within that region.**

---

# 📌 Practical: Create and Mount Amazon EFS (NFS)

## 🔹 Step 1: Create EFS File System  
1. Open **Amazon EFS** in AWS Console.  
2. Click **Create file system**.  
3. Configure:  
   - **Name**: `my-efs`  
   - **VPC**: Select your VPC  
   - **AZs/Subnets**: Choose subnets (for high availability, select multiple AZs).  
4. **Security Groups**: Allow **NFS traffic (port 2049)**.  
5. Click **Create**.  

---

## 🔹 Step 2: Install NFS Utilities on EC2 Instances  

For **Amazon Linux**:  
```bash
sudo yum install -y amazon-efs-utils
```
# AWS EFS Practical Guide  

## 🔹 Step 1: Create an EFS File System  

1. Go to the **AWS Management Console → EFS**.  
2. Click **Create file system**.  
3. Select your **VPC** and Availability Zones (AZs).  
4. Attach **Mount Targets** in each AZ (linked to Subnets & Security Groups).  
5. Set **Performance mode** (General Purpose or Max I/O).  
6. Enable **Encryption** (recommended).  
7. Click **Create**.  

---

## 🔹 Step 2: Install NFS Utilities on EC2 Instances  

For **Ubuntu/Debian**:  
```bash
sudo apt-get update
sudo apt-get install -y nfs-common
```
**For Amazon Linux / RHEL / CentOS**
```sh
sudo yum install -y amazon-efs-utils
sudo yum install -y nfs-utils
```
**🔹 Step 3: Mount the EFS File System**

1.Get your EFS File System ID (e.g., fs-12345678) from the AWS console.
2.Create a mount point:
```sh
sudo mkdir -p /mnt/efs
```
**using NFS protocol**
```sh
sudo mount -t nfs4 -o nfsvers=4.1 fs-12345678.efs.us-east-1.amazonaws.com:/ /mnt/efs
```
**to mount**
```sh
systemctl daemon-reload
mount -a
```
**to verify**
```sh
df -h
```
