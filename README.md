# AWS Public Network Foundation

## Project Overview
This project demonstrates the manual configuration of a foundational AWS networking architecture using the AWS Management Console. It establishes a secure, isolated virtual network capable of hosting public-facing resources, demonstrating core cloud networking concepts.

## Architecture Overview & Resource Map
The network consists of a Virtual Private Cloud (VPC), a Public Subnet, an Internet Gateway (IGW), and a custom Route Table. The Resource Map below visualizes how these components are successfully linked together.

![AWS Resource Map](screenshots/Screenshot%202026-08-03%20231826.png)

## Implementation Details

### 1. Virtual Private Cloud (VPC)
A custom VPC was created to serve as the isolated network environment.
* **Name:** MyProject-VPC
* **IPv4 CIDR:** 10.0.0.0/16

![VPC Details](screenshots/Screenshot%202026-08-03%20232254.png)

### 2. Public Subnet
A subnet was provisioned within the VPC to house public-facing resources.
* **Name:** MyProject-PublicSubnet
* **Availability Zone:** us-east-1a
* **IPv4 CIDR:** 10.0.1.0/24

![Subnet Details](screenshots/Screenshot%202026-08-03%20232345.png)

### 3. Route Table and Internet Gateway Configuration
To make the subnet truly "public," a Route Table was configured to direct all outbound internet traffic (`0.0.0.0/0`) to an attached Internet Gateway. The local route (`10.0.0.0/16`) allows resources within the VPC to communicate with each other.

![Route Table Details](screenshots/Screenshot%202026-08-03%20232543.png)

## Skills Demonstrated
* AWS VPC Creation and Management
* Subnetting and CIDR Block Allocation
* Network Routing and Internet Gateway Attachment
