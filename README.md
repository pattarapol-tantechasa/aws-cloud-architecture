# AWS Cloud Architecture Projects

Two hands-on AWS infrastructure projects built as part of 
Cloud Computing Architecture coursework at Swinburne University.

## Project 1 — Secure VPC with Photo Album Website
**Services:** EC2, RDS (MySQL), S3, VPC, Security Groups, NACLs

- Designed a multi-subnet VPC across 2 availability zones 
  with public/private subnet separation
- Deployed a PHP web app on EC2 with Apache, connected to 
  RDS MySQL and S3 for photo storage
- Configured security groups following least-privilege principle
- Implemented Network ACL to restrict ICMP traffic to specific subnets
- Used bastion host pattern for secure private subnet access

## Project 2 — Highly Available Auto-Scaling Architecture
**Services:** ELB, Auto Scaling Groups, Lambda, S3, RDS, NAT Gateway, IAM, NACLs

- Extended Project 1 into a highly available architecture 
  across multiple availability zones
- Configured Application Load Balancer with target group health checks
- Built Auto Scaling Group (min 2, max 3 instances) with CPU 
  target tracking policy at 30%
- Created Lambda function (Python) triggered by S3 upload 
  to auto-resize images
- Restricted S3 access via bucket policy to ELB origin only
- Applied IAM roles following least-privilege principle across 
  EC2, Lambda, and S3
- Validated NACL blocking bidirectional ICMP from Dev Server 
  to private subnets