<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Kevin  
**Email:** kevinjim2901@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/restful_blue_shy_dragon/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate a cloud security project. I'm doing this project to learn Amazon Virtual Private Cloud (VPC), to create public subnet and an internet gateway. I'm really excited to try cloud services that are actually used in organizations. Let's start !

### What is Amazon VPC?

Amazon VPC is your own isolated, private network within the AWS cloud and it is useful because you can create subnets, control traffic flows and set up security groups.

In today's project, I used Amazon VPC to create subnets, set up internet gateways and configure IP addresses and CIDR blocks.

### Personal reflection

This project took me around 1.5 hours including demo time and quiz.

One thing I didn't expect in this project was it was more faster to use AWS CloudShell to setup VPC , create subnets and internet gateway.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will access the VPC console in AWS selecting the closest region to create a VPC because selecting a distant region increases latency.

### How VPCs work

VPC (Virtual Private Cloud) is a private, isolated section of a public cloud where you can launch resources in a virtual network you define. It gives you control over your network environment, including IP address ranges, subnets, route tables, and network gateways.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because when you create your AWS account, AWS automatically sets up a default VPC. This default VPC is why you could launch resources. If it didn't exist, you would've had to learn how to create a VPC before you can use some of the services that need VPCs to function.

![Image](http://learn.nextwork.org/restful_blue_shy_dragon/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a way to assign a whole block of IP addresses, kind of like creating a zone/area in a city.

---

## Subnets

### What I did in this step

In this step, I will create a subnet to divide this large space into subdivisions. They help organize and secure networks by breaking them into manageable segments, improving efficiency and reducing broadcast traffic.

### Creating and configuring subnets

Subnets are a logical subdivision of an IP network. It helps organize and secure a larger network by dividing it into smaller, manageable segments. There are already subnets existing in my account, one for every Availability Zones (AZs).

### Public vs private subnets

The difference between public and private subnets is that private subnets does not have direct internet access. It is used for internal resources that don’t need to be publicly accessible. For a subnet to be considered public, it has to be connected to the internet. Resources inside a public subnet can communicate with external networks.

![Image](http://learn.nextwork.org/restful_blue_shy_dragon/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 address. This setting makes sure any EC2 instance launched in that subnet will get a public IP address so that I won't have to create one manually.

---

## Internet gateways

### What I did in this step

In this step, I will attach my VPC with an internet gateway because I need to connect my EC2 instance to the internet, so my resources can communicate beyond my private space.

### Setting up internet gateways

Internet gateways are a bridge to connect my VPC to the internet. Internet gateways are key to making applications available on the internet. By attaching an internet gateway, your instances can access the internet and be accessible to external users.

Attaching an internet gateway to a VPC means resources can now access the internet. If I missed this step, my applications hosted on this server will still be private and cannot be accessible on the internet.

![Image](http://learn.nextwork.org/restful_blue_shy_dragon/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will use the AWS CloudShell to setup up my VPC, subnet and internet gateway to check whether it is faster and more efficient way.

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell, which is a shell in your AWS Management Console, to run code. CLI is a software that lets you create, delete and update AWS resources with commands instead of clicking through your console.

### Debugging my setup

To set up a VPC or a subnet, you can use the command  "aws ec2 create-subnet --vpc-id vpc-0b7cb5b82a5a29c18 --cidr-block 10.0.0.0/25". Make sure to avoid errors by including the missing parameters.

![Image](http://learn.nextwork.org/restful_blue_shy_dragon/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is most faster and efficient. An advantage of using the Console is user friendly. Overall, I preferred CloudShell.

---

---
