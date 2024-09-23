+++
title = "Create a CloudFormation stack"
date = "`r Sys.Date()`"
weight = 2
chapter = false
pre = "<b>2.2. </b>"
+++
#### Create a CloudFormation stack

- We will use below file template to create CloudFormation stack. The template defines :
    - A VPC named **CdkStack/DevAxNetworkVPC**:
        - 2 Public Subnet
        - 2 Private Subnet
        - 2 NAT gateways
    - An EC2 Instance named **DevAxWindowsHost**
    - A RDS named **ad12azpxp74wamj**
    - User **awsstudent**

**Template File**
[Module1.yaml](https://000050.awsstudygroup.com/2-prepare/2.2-createstack/_index.files/Module1.yaml) (39 KB)

1. Download file **Module1.yaml**.
2. Go to Amazon CloudFormation Console.
- Click **Stacks**
- Click **Create stack**.



3. In the Specify template section.
- Select Upload a template file
- Click Choose file, then select file Module1.yaml we downloaded.
- Click Next.

4. In the **Stack name** section, type `aws-stack-for-Devax`.

- In the **Stack name** section, seclect `KPforDevAxInstances`.
- Click **Next**.


5. In the **Configure stack options** page, Drag the screen down, then Click **Next**.


6. In the **Review aws-stack-for-Devax** page.
Drag the screen down, then Click **I acknowledge that AWS CloudFormation might create IAM resources with custom names**.
Click **Create stack**.


{{% notice note %}}
Cloudformation will take 5 minutes to deploy Web App. Wait until all stacks are shown in a CREATE_COMPLETE state.
{{% /notice %}}

#### Check the VPC was created
1. Go to [Amazon VPC Console](https://console.aws.amazon.com/vpc/).
- Click **Your VPCs.**
- We will see a VPC named **CdkStack/DevAxNetworkVPC**


2. Click **Subnets**.
- type `CdkStack/DevAxNetworkVPC` into the search bar. Press **Enter**
- We will see 4 Subnets

3. Click **NAT Gateways**.
type `CdkStack/DevAxNetworkVPC` into the search bar. Press **Enter**
We will see 2 NAT gateways
Create CloudFormation stack

#### Check EC2 Instance was created
1. Go to [Amazon EC2 console](https://console.aws.amazon.com/ec2/).
- Click **Instances**.
- type `DevAxWindowsHost` into the search bar. Press **Enter**
- We will see an EC2 Instance named **DevAxWindowsHost**

#### Check AWS RDS was created
1. Go to [Amazon RDS console](https://console.aws.amazon.com/rds/).
- Click Databases.
- We will see new Databases