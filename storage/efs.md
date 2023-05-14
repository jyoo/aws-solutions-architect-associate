# Features
- Two storage classes: Standard and infrequent access
- Performance models: General purpose and Max I/O
- Lifecycle management similar to S3 (standard <-> infrequent access tier)
- NFS (Network File System) version 4 protocol with support of thousands of concurrent NFS connection
- Read after write consistency

## EFS / EBS / FSx for Windows File Server / FSx for Luster
- EC2 instances with Windows cannot use EFS
- EFS is stored across multiple AZ (unlike EBS that stores data in a single AZ)
- EFS can be used by multiple EC2 instances & it does not need any provision
- FSx for Windows File Server is designed for Windows and Windows applications - managed Windows server that use Windows SMB (Server Message Block)
- FSx for Luster is optimized for HPC (High-performance computing). It can store data directly on S3

# Throughput modes
- Bursting throughput: Get more throughput as you store more
- Provisioned throughput

# Security
- Following permissions are needed to configure EFS file system
    - `elasticfilesystem:CreateFileSystem`
    - `elasticfilesystem:CreateMountTarget`
        - `"Resource": "arn:aws:elasticfilesystem:region-id:file-system/*"`
    - `ec2:DescribeSubnet`
    - `ec2:CreateNetworkInterface`
    - `ec2:DescribeNetworkInterfaces`
        - `"Resource": "*"`
- To manage EFS using the AWS management console,
    - `ec2:DescribeAvailabilityZones`
    - `ec2:DescribeSecurityGroups`
    - `ec2:DescribeVpcs`
    - `ec2:DescribeVpcAttribute`
        - To view EFS resources
        - To query EC2 allowing it to display VPCs, AZs and security groups
        - To enable KMS actions if encryption is enabled on the EFS file system
- Encryption of data at rest
    - KMS master key (CMK, Customer Master Key) is required 
        - CMK can generate, encrypt and decrypt data encryption keys (used for other encrpyion in AWS)
    - Type 1 of CMK: managed and created by you or by importing key material from existing key management applications
    - Type 2 of CMK: managed and created by themselves
    - KMS is regional service (cannot be used for multiple regions)

# Additional Notes
