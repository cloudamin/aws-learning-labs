# 🖥️ EC2 User Data Demo

## Overview
This project was created while completing the EC2 section in the AWS Certified Solutions Architect – Associate (SAA-C03) course by Stephane Maarek.  
It demonstrates how to launch an EC2 instance and automatically configure it at boot using **User Data scripts**.

## Steps
1. Launched a t3.micro EC2 instance (Amazon Linux 2023)
2. Added User Data script to install and start a web server
3. Verified that the web page loads automatically after instance launch

## User Data
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from ip-172-31-30-55.ec2.internal </h1>" > /var/www/html/index.html
