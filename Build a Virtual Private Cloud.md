
# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Eduardo Gonzalez  
**Email:** edux2711@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use Amazon VPC and how to create a public subnet and an internet gateway. I'm doing this project to learn AWS cloud infrastructure.

### What is Amazon VPC?

### Personal reflection

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will create a new VPC in the AWS account.

### How VPCs work

VPCs allow resources to be made private to you. It allows accounts to organize resources and have complete control over them.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because services like EC2 and some databases require a VPC to function properly.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a block of IP addresses that resources inside the VPC can use.

---

## Subnets

### What I did in this step

In this step, I will launch a subnet inside the VPC to divide the CIDR block into subnets.

### Creating and configuring subnets

Subnets are groups that divide large IP blocks into smaller ranges to organize resources with similar requirements. There are already subnets existing in my account, one for every Availability Zone.

### Public vs private subnets

The difference between public and private subnets are that public subnets have internet access while private subnets do not. For a subnet to be considered public, it has to have an Internet Gateway set up.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 address. This setting makes sure any EC2 instance created inside the subnet automatically gets a public IP address to avoid wasting time creating one manually.

---

## Internet gateways

### What I did in this step

In this step, I will create an internet gateway to allow the public subnet to access the internet.

### Setting up internet gateways

Internet gateways connect a VPC to the internet.

Attaching an internet gateway to a VPC means that the VPC now has internet access. If I missed this step, the VPC would not be public to users in the internet.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will use AWS CloudShell and run CLI commands to set up a VPC, subnet, and internet gateway faster.

### Exploring CloudShell and CLI

### Debugging my setup

To set up a VPC or a subnet, you can use the command aws ec2. Make sure to avoid errors, including missing to provide a valid CIDR block when creating a subnet.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is the speed and effectiveness. An advantage of using the Console is its simplicity. Overall, I preferred using the CLI because it was faster.

---

---
