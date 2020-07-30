# aws-cloudformation
IaaC to deploy web servers  highly available web application using CloudFormation

## Problem Statement
Your company is creating an Instagram clone called Udagram. Developers pushed the latest version of their code in a zip file located in a public S3 Bucket. You have been tasked with deploying the application, along with the necessary supporting software into its matching infrastructure. This needs to be done in an automated fashion so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.

## Requirements
### Server specifications
1. Create a Launch Configuration for application servers in order to deploy four servers, two located in each of the private subnets. The launch configuration will be used by an auto-scaling group.
2. Two vCPUs, at least 4GB of RAM and 10GB of disk space. The Operating System to be used is Ubuntu 18. 

## Security groups and roles
### Specifications
1. Create an IAM Role that allows EC2 instances to use the S3 Service.
2. Udagram communicates on the default HTTP Port: 80, so servers will need this inbound port open since it will be used with the Load Balancer and the Load Balancer Health Check. As for outbound, the servers will need unrestricted internet access to be able to download and update its software.
3. The load balancer should allow all public traffic (0.0.0.0/0) on port 80 inbound, which is the default HTTP port. Outbound, it will only be using port 80 to reach the internal servers.

4. The application needs to be deployed into private subnets with a Load Balancer located in a public subnet.
5. One of the output exports of the CloudFormation script should be the public URL of the LoadBalancer. Bonus points for adding http:// in front of the load balancer DNS Name in the output, for convenience.

## Usage
./create.sh your-stack-name stack-infra.yml infra_parameters.json
