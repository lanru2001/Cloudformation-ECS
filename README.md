## Provision the following using cloudformation:

- VPC and basic networking namely an Internet Gateway, public subnet, and route table
- Elastic IP and associate it to an Elastic Network Interface - this will facilitate reuse of the same public IP when the Spot instances terminate
- security groups for Web and SSH access and access from the EC2 instances to EFS
- EFS and a mount point
- ECS Task Definition which defines the required containers and their configurations - this includes mounting the EFS volume into the NGINX container so it can access the Let’s Encrypt files (see omission notes below)
- ECS Cluster and Service
- Auto Scaling Target and Auto Scaling Group which maintains 1 Spot instance for ECS
- Launch Template which configures the Spot Instance/s
- Create the roles required for everything to work correctly
- Configure SNS topic for email notifications when events occur in the Auto Scaling Group


![image](https://user-images.githubusercontent.com/59709429/147859046-9644dbf1-fa19-45b3-97ff-f6347c2ca4d6.png)
