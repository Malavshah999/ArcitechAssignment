# ArcitechAssignment

### Step1. EC2 Instance
- Launched a `t2.micro` instance using Ubuntu AMI with a lower version 22.04 LTS.
- Installed Python, Git, nginx and gunicorn, pip.

### Step2. Create a  Application
- Created a simple Flask application used source code from google.
- Made required changes nginx for the application.

### Step3. Create a S3 Bucket
- Created an S3 bucket namely devops-assignment-malav-shah  and uploaded a file named find_me_here_malav.txt.

### Step4. Create a CI/CD Pipeline (used Github Action)
- Using Github actions created a workflow to deploy the flask application.

### Step5. Create IAM Roles for Security
- Configure IAM role to allow EC2 to access the S3 bucket.
- Configure 2 more roles to allow Lambda to start EC2 instance and one to stop.

### Step6. Creating a Cron Job
- Createing a cron job to see application health check every 5 minutes.

### Step7. Using lambda to Schedule EC2
- Used AWS Lambda with the CloudWatch Events to schedule EC2 instance start, stop.
