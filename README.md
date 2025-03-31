# Aws-vpc-practice
VPC Setup Guide

Overview

This setup creates a Virtual Private Cloud (VPC) with subnets in different Availability Zones, ensuring high availability and controlled network access. A NAT Gateway allows private instances to access the internet securely, while Security Groups and NACLs provide additional traffic control.

Steps

Create a VPC – This acts as the network boundary where all resources will be deployed.

Set up Subnets – Public subnets are for resources needing internet access, while private subnets are isolated for security.

Attach an Internet Gateway – This enables internet access for instances in the public subnet.

Deploy a NAT Gateway – Placed in the public subnet, it allows instances in private subnets to reach the internet for updates while blocking inbound traffic.

Configure Routing Tables – Public subnets route through the Internet Gateway, and private subnets route outbound traffic via the NAT Gateway.

Set up Security Groups & NACLs – Security Groups control traffic at the instance level, while NACLs define subnet-wide rules.

Testing

Public subnet instances should have direct internet access.

Private subnet instances should reach the internet via the NAT Gateway but remain inaccessible from the public internet.
