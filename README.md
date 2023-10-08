![private-subnet](https://github.com/divyasharma82/AWS-VPC/assets/122516735/51caf24c-0c52-44ec-af60-5737f3412ada)# AWS-VPC
"Welcome to my AWS VPC Learning Repository🌐:, designed to demonstrate my practical expertise in Amazon Virtual Private Cloud (VPC) on AWS.🏢🚀🔒

# My AWS VPC Learning Journey 🌐

## Overview
Welcome to my journey of exploring Amazon Virtual Private Cloud (VPC) on AWS. In this repository, I document my hands-on experience with VPC, including creating VPCs, subnets, route tables, gateways, Network ACLs, VPC Peering, and VPC Endpoints.

## Table of Contents
1. [Lab 1: Creating a VPC, Subnet, and Route Table](#lab-1-creating-a-vpc-subnet-and-route-table)
2. [Lab 2: Setting Up a NAT Gateway](#lab-2-setting-up-a-nat-gateway)
3. [Lab 3: VPC Peering (Cross-Region)](#lab-3-vpc-peering-cross-region)
4. [Lab 4: Network ACLs (NACLs)](#lab-4-network-acls-nacls)
5. [Lab 5: VPC Endpoint](#lab-5-vpc-endpoint)

## Lab 1: Creating a VPC, Subnet, and Route Table

### Step 1: Create a VPC
1. Open the AWS Management Console.
2. Navigate to the VPC Dashboard.
3. Click on "Create VPC."
4. Fill in the VPC details, such as the name and IP address range.
5. Click "Create VPC."
 ![vpc](https://github.com/divyasharma82/AWS-VPC/assets/122516735/8f3a6478-c380-4db4-a167-11585d15043f)


### Step 2: Create Subnets

1. Inside your newly created VPC, navigate to "Subnets."
![subnet](https://github.com/divyasharma82/AWS-VPC/assets/122516735/37d99f5c-850f-4e89-a72e-4137ae4b3484)
2. Click on "Create Subnet."
3. Fill in the subnet details, including the VPC, subnet range, and availability zone.
4. Repeat this step to create additional subnets.

### Step 3: Create a Route Table

![route-able](https://github.com/divyasharma82/AWS-VPC/assets/122516735/d2d07074-c744-431c-9b2d-113b686b6e0b)
1. In the VPC dashboard, go to "Route Tables."
2. Click "Create Route Table."
3. Provide a name and select your VPC.
4. Edit the route table to add routes for the subnets.
5. Associate the route table with your subnets.

### Step 4: Internet Gateway

![igw](https://github.com/divyasharma82/AWS-VPC/assets/122516735/3aa5f13f-da80-45f9-8418-3996e63c1654)
1. In the VPC dashboard, go to "Internet Gateways."
2. Click "Create Internet Gateway."
3. Attach the Internet Gateway to your VPC.
4. Update the route table to route traffic to the Internet Gateway.

## Lab 2: Setting Up a NAT Gateway

### Step 1: Create a NAT Gateway
![natgateway](https://github.com/divyasharma82/AWS-VPC/assets/122516735/0c74d43e-5e36-43cd-ba36-e2ecdc081bae)

1. In the VPC dashboard, go to "NAT Gateways."
2. Click "Create NAT Gateway."
3. Choose the public subnet and allocate an Elastic IP address.
4. Create the NAT Gateway.

### Step 2: Modify Route Tables
![private-subnet](https://github.com/divyasharma82/AWS-VPC/assets/122516735/f12512d3-0cc9-4576-910a-31263b7349c1)
1. Update the route tables for your private subnets to route traffic to the NAT Gateway.

## Lab 3: VPC Peering (Cross-Region)

![vpc-peering](https://github.com/divyasharma82/AWS-VPC/assets/122516735/82dfe564-8dae-4618-ac4c-1d46afd9ae8c)

### Step 1: Create VPCs
1. In both regions, create two VPCs: one in each region.
2. Note the VPC IDs.

### Step 2: Create a VPC Peering Connection
1. In the VPC dashboard, go to "Peering Connections."
2. Click "Create Peering Connection" in one of the VPCs.
3. Specify the other VPC as the peer and approve the request.
   
![accept-vpc-peering](https://github.com/divyasharma82/AWS-VPC/assets/122516735/42861578-be61-4ec4-8f9f-568f45cdfefb)

### Step 3: Update Route Tables
1. In each VPC, update the route tables to include routes for the other VPC's CIDR block, pointing to the VPC Peering Connection.
![vpc-peering-route-table](https://github.com/divyasharma82/AWS-VPC/assets/122516735/4908a096-5b6d-417f-a69f-e0149afe112c)

## Lab 4: Network ACLs (NACLs)

### Step 1: Create a Network ACL
1. In the VPC dashboard, go to "Network ACLs."
2. Click "Create Network ACL."
3. Associate it with your VPC.

### Step 2: Define Rules
1. Edit the Network ACL and define inbound and outbound rules to control traffic between subnets.
2. Associate the Network ACL with the desired subnets.

## Lab 5: VPC Endpoint

![vpc-endpoint](https://github.com/divyasharma82/AWS-VPC/assets/122516735/6f7122c7-e76c-4d5d-86fa-056c0d48e144)

### Step 1: Create a VPC Endpoint
1. In the VPC dashboard, go to "VPC Endpoints."
2. Click "Create Endpoint."
3. Select the service you want to access privately (e.g., S3, DynamoDB).
4. Choose your VPC and routing preferences.

These labs cover a wide range of VPC-related topics and practical usage scenarios. Feel free to explore and adapt these instructions as you explore the world of AWS VPCs. 🌐🏢🚀🔒
