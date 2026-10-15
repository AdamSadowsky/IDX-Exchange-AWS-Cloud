
# Week 3 - EC2 Deployment Runbook

## 1. Create EC2 Instance
- Opened AWS EC2 Console.
- Selected Amazon Linux 2023.
- Chose t3.micro as the instance type.

## 2. Configure SSH
- Selected the training-key RSA key pair.
- Configured the security group to allow SSH on port 22 from my IP.

## 3. Configure Networking
- Allowed TCP traffic on port 8080 for the Flask application.

## 4. Deploy Application
- Added a User Data script that installs Python and Flask.
- Configured the script to create the application files and start Flask automatically.

## 5. Verify Deployment
- Connected to EC2 using SSH.
- Tested the health endpoint:
  curl http://<public-ip>:8080/health
- Confirmed the response was {"status":"ok"}.

## 6. Create EBS Snapshot
- Created a snapshot of the EC2 instance's root EBS volume.
- Verified the snapshot reached Completed status.

## 7. Cleanup
- Terminated the EC2 instance after completing the lab.
