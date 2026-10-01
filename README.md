# AWS EC2 Hands-On Assignment

## Task 1: Launch an EC2 Instance and SSH into It

### Objective

The objective of this task was to launch an Ubuntu EC2 instance on AWS and connect to it remotely using SSH.

### What I Did

1. Logged into the AWS Management Console.
2. Opened the Amazon EC2 service.
3. Launched an Ubuntu EC2 instance.
4. Selected the `t3.micro` instance type.
5. Selected the `Demo` key pair for SSH authentication.
6. Configured the Security Group to allow SSH traffic on port 22.
7. Obtained the public IPv4 address of the EC2 instance.
8. Used Ubuntu WSL and OpenSSH to connect to the instance.
9. Successfully logged into the Ubuntu EC2 server.

### SSH Connection

I connected to the EC2 instance from Ubuntu WSL using:

```bash
ssh -i ~/Demo.pem ubuntu@98.90.195.72

The SSH connection was successful and displayed the Ubuntu welcome message.

What I Learned
EC2 provides virtual servers in the AWS cloud.
SSH allows me to securely connect to a remote Linux server.
Port 22 is the default SSH port.
Security Groups control network access to an EC2 instance.
An SSH private key is required to authenticate with the EC2 instance.
Private SSH keys must have secure file permissions.
WSL can be used to connect to AWS EC2 instances using OpenSSH.
The public IPv4 address is used to connect to the EC2 instance from the internet.
Difficulties Faced

Initially, my SSH connection timed out.

I checked the EC2 networking configuration, including the Security Group and Network ACL.

The Security Group was temporarily changed to allow SSH traffic from 0.0.0.0/0 for troubleshooting. After this change, port 22 became reachable.

I also experienced a private key permission error when attempting to use the WSL private key through Windows OpenSSH.

The error was resolved by using the private key directly from the Ubuntu WSL terminal.

Result

The EC2 instance was successfully launched and I successfully connected to it using SSH from Ubuntu WSL.

Screenshot

The screenshot below shows the successful SSH connection to the Ubuntu EC2 instance.

**Important:** The final screenshot section uses the actual file you copied:

```text
screenshots/EC2 Connection.png
