# Aws-Project
AWS Challenge: 

AWS Challenge: Designing a Robust Web Application on AWS

🔹 *Author*: Riyan Uddin

---

### *Situation*:
In the rapidly evolving world of cloud computing, ensuring high availability and reliability for web applications is crucial. My challenge was to design a robust web application architecture on AWS that would meet these needs.

### *Task*:
The goal was to create a secure, scalable, and highly available web application architecture using various AWS services. This involved configuring a VPC, setting up EC2 instances, deploying a load balancer, and integrating a managed database service (RDS).

### *Action*:

### *Part 1: VPC Configuration*
- *Create VPC*: awsProject-vpc with CIDR block 20.0.0.0/20.
- *Public Subnets*: web-pub-sub1 (20.0.1.0/24, us-east-1a), web-pub-sub2 (20.0.2.0/24, us-east-1b).
- *Private Subnets for Applications*: app-pvt-sub1 (20.0.3.0/24, us-east-1a), app-pvt-sub2 (20.0.4.0/24, us-east-1b).
- *Private Subnets for Databases*: db-pvt-sub1 (20.0.5.0/24, us-east-1a), db-pvt-sub2 (20.0.6.0/24, us-east-1b).
- *NAT Gateway*: my-nat in web-pub-sub1 with Elastic IP.
- *Internet Gateway*: my-igw attached to awsProject-vpc.
- *Route Tables*: route-web, route-app, route-db with appropriate subnet associations and routes.

### *Part 2: EC2 Instances Setup*
- *Jump Server*: Launched in the public subnet web-pub-sub1 with public IP for secure access.
- *App Servers*: Deployed in private subnets app-pvt-sub1 and app-pvt-sub2 without public IPs. Installed PHP 8.2, Apache, and phpMyAdmin.
- *Security Groups*: Configured to allow necessary traffic (SSH, HTTP).

### *Part 3: Load Balancer & RDS Configuration*
- *Load Balancer*: Created an Internet-facing ALB with target group app-tg to distribute traffic evenly.
- *RDS Setup*: MySQL instance configured with the appropriate subnet group and security group. Updated phpMyAdmin to connect to the RDS instance.

### *Result*:
By visiting the load balancer DNS, users can access the application, which demonstrates successful load balancing between servers. The architecture ensures high availability and redundancy, providing a reliable user experience. This project underscores the flexibility and robustness of AWS for building scalable web applications.

---

### *Outcome*:
Successfully designed and deployed a highly available and secure web application architecture on AWS, enhancing my cloud computing skills and knowledge.

🛠️ *Key Services Used*:
- Route 53
- VPC
- EC2
- NAT Gateway
- Internet Gateway
- ALB
- RDS

---

### This project highlights the power of AWS in creating scalable, high-availability web applications. Huge thanks to Riyan Uddin for the guidance and support throughout this challenge!


#AWS #CloudComputing #WebDevelopment #EC2 #RDS #DevOps #VPC #LoadBalancing #Scalability #HighAvailability #AWSChallenge
