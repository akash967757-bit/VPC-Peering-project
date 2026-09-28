# AWS VPC Peering Project

## Project Overview

This project demonstrates how to establish private network communication between two Amazon VPCs using VPC Peering.

## AWS Services Used

* Amazon VPC
* Amazon EC2
* VPC Peering
* Route Tables
* Security Groups

## Network Configuration

### VPC 1

* CIDR: `10.0.0.0/16`
* EC2 Private IP: `10.0.1.10`

### VPC 2

* CIDR: `20.0.0.0/16`
* EC2 Private IP: `20.0.1.10`

## Project Flow

```text
VPC 1
10.0.0.0/16
     |
   EC2-1
     |
VPC Peering
     |
   EC2-2
     |
VPC 2
20.0.0.0/16
```

## Implementation Steps

1. Created VPC 1 with CIDR `10.0.0.0/16`
2. Created VPC 2 with CIDR `20.0.0.0/16`
3. Launched EC2 instances in both VPCs
4. Created a VPC Peering Connection
5. Accepted the peering request
6. Added routes to both VPC route tables
7. Updated Security Group rules
8. Tested private connectivity between the EC2 instances

## Connectivity Test

The connectivity was tested using the private IP address of the EC2 instance in the peered VPC.

Example:

```bash
ping 20.0.1.10
```

## Key Learning

* VPC networking
* CIDR and private IP addressing
* VPC Peering
* Route Table configuration
* Security Groups
* Private communication between VPCs

## Result

Successfully established private communication between two separate AWS VPCs using VPC Peering.

