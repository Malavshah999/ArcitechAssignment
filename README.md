# ArcitechAssignment

### Step1. EC2 Instance
- Launched a `t2.micro` instance using Ubuntu AMI with a lower version 22.04 LTS.
- Installed Python, Git, nginx and gunicorn, pip using command
`sudo apt-get install python3 python3-pip nginx git -y`
`sudo pip3 install flask`
`sudo pip3 install gunicorn`

### Step2. Create a  Application
- Created a simple Flask application used source code from google mentioned in above file.
- Made required changes nginx for the application.
- Run the application using command `gunicorn --workers 3 --bind 0.0.0.0:8000 app:app`
- Modify nginx proxy at `/etc/nginx/sites-available/flask_app`

### Step3. Create a S3 Bucket
- Created an S3 bucket namely devops-assignment-malav-shah  and uploaded a file named find_me_here_malav.txt.
- Set the bucket to allow public read access. 

### Step4. Create a CI/CD Pipeline (used Github Action)
- Using Github actions created a workflow to deploy the flask application after installing required tools/libraries (gunicorn, python etc.)

### Step5. Create IAM Roles for Security
- Configure IAM role to allow EC2 to access the S3 bucket.
- Attach the Role to Your EC2 Instance
- Configure 2 more roles to allow Lambda to start EC2 instance and one to stop.

### Step6. Creating a Cron Job
- Create a bash script and make it executable.
- Createing a cron job to see application health check every 5 minutes.

### Step7. Using lambda to Schedule EC2
- Used AWS Lambda with the CloudWatch Events to schedule EC2 instance start, stop.
- Majorly referred multiple AWS documentation and Udemy lectures by Stephen Maarek.
