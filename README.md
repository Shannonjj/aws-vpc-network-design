# AWS VPC Network Design and Builds

Three virtual private cloud builds from my UMGC coursework, covering manual design, a scored hands-on lab, and IP subnetting design work.

## 1. Manual VPC Build for Cloud Backup Deployment (CCA 630)
Built a VPC piece by piece in the AWS console as the network foundation for a NetApp Cloud Sync backup deployment:
- VPC **cca630VPC** — CIDR **10.0.0.0/26**
- Four subnets (public and private, /28 each) across availability zones: cca630-public-a/c and cca630-private-a/c
- Separate **public and private route tables** with explicit subnet associations
- **Internet Gateway** (cca630IGW) attached, with a 0.0.0.0/0 route on the public route table
- Auto-assign public IPv4 and DNS hostnames configured
- The private subnet was designed to host the VPN connection and the Cloud Sync data broker path to Amazon S3

## 2. Introduction to Amazon VPC Lab (Qwiklabs) — Score: 100/100
- Built a VPC with public and private subnets using the VPC wizard: **10.0.0.0/16**, public subnet 10.0.25.0/24, private subnet 10.0.50.0/24 (us-east-1a)
- Allocated an **Elastic IP** and created a **NAT gateway** for private-subnet outbound access; private route table points 0.0.0.0/0 to the NAT gateway
- Verified route tables, network ACL rules (inbound/outbound), and security groups

## 3. Subnetting Design — BallotOnline (CCA 625, coursework case study)
- Designed a subnet plan for network **172.16.192.0/19**, carving it into subnets for four field offices
- Calculated network IDs, broadcast addresses, and usable IP ranges by hand (work shown in the project worksheets)

## Skills demonstrated
- Amazon VPC, subnets, route tables, Internet Gateways, NAT gateways, Elastic IPs
- IPv4 subnetting and CIDR design
- Network ACLs and security groups


---
*Shannon Javone Jenkins — MS in Cloud Computing Architecture, University of Maryland Global Campus (UMGC). Graduate coursework and hands-on labs.*
