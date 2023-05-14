# Features
- EBS: Elastic Block Store - Persistent block storage volumes for EC2
- Logically attached and physically separated from an EC2 instance
- Automatic replication to other EBS volumes within the same AZ
    - Recreating a volume using snapshot and attaching it to EC2 in another AZ is recommended to avoid data loss
- You can connect to or disconnect from EC2s without data loss
- Encryption and snapshot back-up to S3

## EBS vs EFS 
- Review efs.md