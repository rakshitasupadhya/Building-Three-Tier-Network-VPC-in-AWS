# Building-Three-Tier-Network-VPC-in-AWS
This is a demonstartion on building 3 Tier Network using VPC, subnets, Route tables, InternetGateway, NAT Gateway.

# Overview of each component
1. VPC: A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can specify an IP address range for the VPC, add subnets, add gateways, and associate security groups.
2. Subnets: A subnet is a range of IP addresses in your VPC. You launch AWS resources, such as Amazon EC2 instances, into your subnets. You can connect a subnet to the internet, other VPCs, and your own data centers, and route traffic to and from your subnets using route tables.
3. Route Tables: A route table contains a set of rules, called routes, that determine where network traffic from your subnet or gateway is directed.
4. Internet Gateway: An Internet Gateway is a logical connection between an AWS VPC and the Internet. It allows for internet traffic to actually enter into a VPC
5. NAT Gateway: A NAT gateway is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.

# Implementation
1.	Create only VPC
2.	Create 6 subnets – 2 DMZpublic, 2 Applayer private, 2 DBlayer private
3.	Create Internet Gateway to connect public subnets to open internet
4.	Create NATGateway
5.	Create Public & private Route tables
6.	Associate public RT to public subnets
7.	Associate private RT to private subnets
8.	To public RT add route to Internet gateway 
9.	To private RT add route to NAT gateway
10.	Create NACL for 3 layers- DMZ, applayer,dblayer
11.	Associate NACL to respective subnets 

