# Project-lab17-hybridapp-onboarding
Hands-on project: Hybrid App Onboarding &amp; Configuration using SSH and SCP on AWS EC2 (Linux 2023). Demonstrates secure file transfer, key pair authentication, and Linux environment prep.
Lab 17: Hybrid App Onboarding & Configuration on AWS EC2
1. Introduction
This lab focuses on securely onboarding a hybrid application onto an Amazon EC2 instance using SSH key-pair authentication and file transfers via SCP. The goal is to simulate a secure hybrid app deployment in the cloud environment using real-world tools like Git Bash, AWS EC2, and SCP for file transfer. This lab is part of a series of advanced AWS Cloud Security projects, and it showcases practical DevSecOps skills including secure access configuration, file permissions, and deployment preparation.
2. Objectives
- Launch and access an Amazon EC2 instance using SSH.
- Transfer the hybrid application folder from local machine to EC2.
- Ensure permission integrity and path correctness.
- Prepare the environment for further deployment in a secure hybrid setup.
3. Tools & Technologies Used
- AWS EC2 (Amazon Linux 2023)
- Git Bash (Windows)
- Secure Copy Protocol (SCP)
- SSH (with .pem key)
- Local PC (Windows 10)
4. Lab Execution Steps
Step 1: Launch EC2 Instance
An EC2 instance running Amazon Linux 2023 was launched. A key-pair was generated and downloaded locally for SSH access.
Step 2: Prepare PEM File
The .pem file (project_lab17-hybridapp-instance.pem) was moved to a secure location on the local machine, specifically in C:/Users/IME-PC.
Step 3: Package and Locate Hybrid App
The hybrid application folder was placed in the same directory to ensure simple navigation and compatibility with SCP.
Step 4: SCP Transfer to EC2
Using the following command, the entire folder was transferred securely to the EC2 instance:

scp -i /c/Users/IME-PC/project_lab17-hybridapp-instance.pem -r /c/Users/IME-PC/hybrid-app ec2-user@34.231.240.48:~/hybrid-app
Step 5: SSH into EC2
After the successful transfer, SSH access was established:

ssh -i /c/Users/IME-PC/project_lab17-hybridapp-instance.pem ec2-user@34.231.240.48
Step 6: Verification
Within the EC2 instance, the hybrid-app directory was confirmed to be present, and contents were verified using:

cd hybrid-app && ls
5. Challenges Faced
- PEM file permission denied due to wrong path.
- SCP failed due to misplacement of hybrid-app folder.
- Mistakes in initial SCP and SSH path formatting.
- Required file relocation to ensure successful execution.
6. Final Result
The hybrid application folder was securely transferred and stored in the EC2 instance. This setup is now ready for secure application deployment in future labs. All operations were executed using the Linux terminal (Git Bash), and permissions were confirmed. The lab validates the learner's ability to perform real-world DevSecOps operations.
7. CV/Resume Experience Entry
Hybrid App EC2 Onboarding Lab – AWS (Lab 17)
- Configured SSH access to EC2 using secure key-pairs.
- Transferred and validated hybrid app components using SCP.
- Troubleshot permission and path issues for secure file handling.
- Prepared instance for multi-environment hybrid application deployment.
- Demonstrated DevSecOps principles using Linux and AWS.
8. GitHub README Template
```markdown
# Lab 17: Hybrid App Onboarding & EC2 Setup

## Objectives
- SSH into EC2 instance securely
- Use SCP to upload application files
- Prepare for cloud deployment

## Tools Used
- AWS EC2 (Amazon Linux 2023)
- Git Bash on Windows
- SSH + SCP

## Key Commands
ssh -i /path/to/key.pem ec2-user@<Public-IP>
scp -i /path/to/key.pem -r /path/to/app ec2-user@<Public-IP>:~/destination-folder

## Result
Hybrid app folder securely transferred and ready for deployment
```

| Field                           | Detail                                                                               |
| ------------------------------- | ------------------------------------------------------------------------------------ |
| **Author Name**                 | Dr. Ime Ben                                                                          |
| **GitHub Username**             | [ime-cloud-sec-analyst](https://github.com/ime-cloud-sec-analyst)                    |
| **Title**                       | AWS Cloud Security Engineer / DevSecOps Engineer                                     |
| **Email (optional for README)** | [imegcu55@gmail.com](mailto:imegcu55@gmail.com)                                      |
| **Location**                    | Glasgow, United Kingdom                                                              |
| **GitHub Portfolio**            | [https://github.com/ime-cloud-sec-analyst](https://github.com/ime-cloud-sec-analyst) |
| **Certifications**              | AWS Security Specialty, Terraform Associate, Azure Security Engineer                 |
| **Tools & Tech**                | AWS, Terraform, GitHub Actions, Linux, Splunk, SIEM, SCP, SSH, EC2, IAM              |
| **LinkedIn (optional)**         | (Add your LinkedIn link if you want to share)                                        |
| **License Contributor**         | Yes, licensed under \[MIT License] unless otherwise stated                           |
