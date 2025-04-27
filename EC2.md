# Amazon EC2 (Elastic Compute Cloud)

## What is EC2?
- Infrastructure as a Service (IaaS)
- Rent virtual machines
- Store data on virtual drives (EBS)
- Distribute load across machines (ELB)
- Scale services using Auto Scaling Groups (ASG)

## EC2 Configuration Options
- Operating System (Linux, Windows, Mac OS)
- CPU and number of cores
- RAM
- Storage (EBS or Instance Store)
- Network card
- Security Groups (firewall rules)
- EC2 User Data (bootstrapping commands)

## EC2 User Data
- Script runs at instance launch
- Used for:
  - Installing software
  - Updating OS
  - Downloading files
- Runs as root user

## EC2 Instance Types
- General Purpose (e.g., t2.micro)
- Compute Optimized
- Memory Optimized
- Storage Optimized
- Naming Example: `m5.2xlarge`
  - m: instance class
  - 5: generation
  - 2xlarge: size

## EC2 Purchasing Options
- On-Demand Instances
  - Pay per second, highest flexibility
- Reserved Instances
  - 1 or 3 years commitment, big discount
- Savings Plans
  - Commit to $/hour usage, flexibility
- Spot Instances
  - Up to 90% discount, can be interrupted
- Dedicated Hosts
  - Physical server reserved for you
- Dedicated Instances
  - Hardware isolation, no control over placement
- Capacity Reservations
  - Reserve capacity in a specific AZ

## Security Groups
- Virtual firewall for instances
- Control inbound and outbound traffic
- Rules based on IP, port, or security group
- All inbound traffic is blocked by default
- All outbound traffic is allowed by default

## Classic Ports to Know
- 22: SSH (Linux login)
- 21: FTP
- 22: SFTP (over SSH)
- 80: HTTP (web traffic)
- 443: HTTPS (secure web traffic)
- 3389: RDP (Windows login)

## SSH Access Methods
- Mac/Linux: Terminal (SSH command)
- Windows < 10: PuTTY
- Windows ≥ 10: Windows Terminal (SSH native)
- EC2 Instance Connect (browser-based SSH)

## EC2 Instance Storage
- EBS (Elastic Block Store)
  - Network drive
  - Persistent
  - AZ-locked
  - Snapshots available
- EC2 Instance Store
  - Physical disk attached to host
  - High performance
  - Lost if instance stops
- Elastic File System (EFS)
  - Mount across multiple instances
  - Works in multiple AZs
  - Expensive but scalable

## EBS Snapshots
- Backup EBS volume at a point in time
- Copy across AZs and Regions
- Archive tier (75% cheaper, slower restore)
- Recycle Bin for deleted snapshots

## AMI (Amazon Machine Images)
- Pre-configured OS + software bundle
- Can create custom AMI from instance
- Public, Private, or AWS Marketplace AMIs
- Can be copied across Regions

## EC2 Image Builder
- Automate creation of custom AMIs
- Define build and test pipelines
- Free service (only pay for resources used)

## Shared Responsibility Model for EC2
### AWS responsibility:
- Physical security
- Infrastructure maintenance
- Isolation of instances

### Customer responsibility:
- Security Groups
- OS patching
- Data encryption
- IAM roles on EC2
- Application security
