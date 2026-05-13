my-second project

AWS Cloud Implementation for Web Hosting – Project Notes


## About This Project
1. Project Overview
The project focuses on hosting a scalable and highly available web application using Amazon Web Services (AWS). The solution leverages core AWS services to ensure reliability, security, performance, and cost efficiency when deploying a public-facing website.

2. Objectives

·	Host a web application on the AWS cloud
·	Achieve high availability and scalability
·	Implement secure access and networking
·	Enable monitoring and fault tolerance
·	Optimise operational and infrastructure costs


3. AWS Services Used
·	Compute

i.	Amazon EC2 – Provides virtual servers to host the web application.
ii.	Auto Scaling Groups – Automatically adjusts the number of EC2 instances based on load.

·	Networking

i.	Amazon VPC – Isolated virtual network for hosting resources.
ii.	Public Subnet – Hosts EC2 web servers exposed to the internet.
iii.	Private Subnet – Used for databases or backend services.
iv.	Internet Gateway – Enables internet access.
v.	Security Groups & Network ACLs – Control inbound and outbound traffic.

·	Load Balancing

i.	Elastic Load Balancer (ALB) – Distributes traffic across multiple EC2 instances to ensure high availability.

·	Storage

i.	Amazon S3 – Stores static web content, images, and backups.
ii.	Elastic Block Store (EBS) – Persistent storage for EC2 instances.

·	Database

i.	Amazon RDS (MySQL/PostgreSQL) – Managed relational database with automated backups and scaling.

·	DNS & Content Delivery

i.	Amazon Route 53 – Domain management and DNS routing.
ii.	Amazon CloudFront – Content Delivery Network (CDN) for faster global content delivery.

·	Security & Identity

i.	IAM (Identity and Access Management) – Manages users, roles, and permissions.
ii.	AWS Certificate Manager – Enables HTTPS via SSL/TLS certificates.

·	Monitoring & Management

i.	Amazon CloudWatch – Monitors system metrics and logs.
ii.	AWS CloudTrail – Tracks API activity for auditing and compliance.


4. Architecture Flow

·	User accesses the website via a domain name (Route 53).
·	Traffic is routed through an Application Load Balancer.
·	Load Balancer distributes traffic to EC2 instances.
·	EC2 instances fetch static data from S3 and dynamic data from RDS.
·	CloudWatch monitors performance and triggers Auto Scaling if required.


5. Implementation Steps (High-Level)

·	Create a VPC with public and private subnets
·	Configure Internet Gateway and routing tables
·	Launch EC2 instances with a web server (Apache/Nginx)
·	Deploy the website code
·	Configure Load Balancer and Auto Scaling
·	Set up RDS in a private subnet
·	Enable monitoring, logging, and security policies


6. Security Considerations

·	Least‑privilege IAM roles
·	HTTPS enabled using SSL certificates
·	Private database subnets
·	Restricted inbound rules in security groups
·	Regular backups and monitoring


7. Advantages of Using AWS

·	High availability and fault tolerance
·	On‑demand scalability
·	Pay‑as‑you‑go pricing
·	Global infrastructure
·	Built‑in security and compliance features


8. Conclusion
This AWS-based web hosting solution provides a robust, scalable, and secure platform for deploying modern web applications. It demonstrates effective use of cloud computing concepts such as elasticity, automation, and high availability.


## What's Inside
- README.md — this file
- project-notes.txt — my project notes

## Author
Made with ❤️ by **priya**
