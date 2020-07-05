# aws-cloudformation-udacity
IaaC to deploy web servers  highly available web application using CloudFormation

## Problem Statement
Your company is creating an Instagram clone called Udagram. Developers pushed the latest version of their code in a zip file located in a public S3 Bucket. You have been tasked with deploying the application, along with the necessary supporting software into its matching infrastructure. This needs to be done in an automated fashion so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.

## Requirements
### Server specifications
1. Create a Launch Configuration for application servers in order to deploy four servers, two located in each of the private subnets. The launch configuration will be used by an auto-scaling group.
2. Two vCPUs, at least 4GB of RAM and 10GB of disk space. The Operating System to be used is Ubuntu 18. 
