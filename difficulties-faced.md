## Introduction

This document mentions the difficulties I faced, the resources I used for help, and the solutions I used to resolve errors.

### 1. Setting Lambda Functions
To Set up AWS Lambda functions to start and stop EC2 instances presented a few challenges as I am currently learning and honing my skills on AWS SAA. Initially, I struggled a bit to create IAM role with the correct permissions. Then O referred a few documents and got to know the required policies and role I had to use.

**The Resources I Used:**
- [AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- [AWS IAM Policies and Permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html)

### 2. Configuring the CloudWatch
As I mentioned earlier, I have not been through cloudwatch so I also faced a few difficulties in setting up CloudWatch events to trigger the Lambda function. Creatong correct pattern for cron took some few minutes but it worked well.

**Resources which were used:**
- [Amazon CloudWatch Events](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/WhatIsCloudWatchEvents.html)
- [Creating CloudWatch Events Rules](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/Create-CloudWatch-Events-Rule.html)
- Lectures by Stephen Maarek on udemy.

### 3. EC2 Instance Setup
While setting up the EC2 instance, I mistakenly added a security group rule that allowed inbound traffic from a my own IP address, which was not intended. This caused unnecessary security issue and took some time to be corrected.

**Problem Encountered:**
- Added a security group rule allowing inbound traffic from IP eg.`192.168.0.0/16` instead of anywhere `0.0.0.0`.

## Solutions I Implemented

### 1. Correcting IAM Role Permissions
To resolve the issues with the IAM role, I revisited the AWS documentation and ensured the role had the necessary policies attached. I used the AWS Management Console to verify and attach the `AWSLambdaBasicExecutionRole` and `AmazonEC2FullAccess` policies.

### 2. Configuring Correct Cron *
I used the AWS documentation on CloudWatch Events to understand cron expressions better. I also utilized online cron expression generators to ensure the schedules were set correctly.

### 3. Fixing Security Group Rules
To correct the security group rule, I modified the inbound rules to only allow the intended IP.

## Efforts and Learning
Throughout this assignment, I put in significant effort to understand and implement AWS Lambda, CloudWatch. The challenges I faced required me to consult various AWS documentation and external resources, which improved my understanding of these services. By resolving these issues, I gained good experience and improved my skills w.r.t AWS resources.

