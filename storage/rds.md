# Features
- RDS supports: Aurora, MySQL, Postgres, Oracle, SQL Server, Maria
- Multi AZ
- Customizable storage threshold related to auto scaling (100 to 65,536 GB)
- Various pricing models: On-demand, On-demand (w/ BYOL), Reserved, Reserved (w/ BYOL), Serverless

# Types
- General purpose SSD storage
- Provisioned IOPS SSD stroage
- Magnetic storage: It supports backward compatibility

# Scaling
- Vertical and horizontal scaling
- Read replica
    - When a read replica is about to be created, a snapshot of db (secondary db if multi AZ is enabled) is taken, and the generated read replica is asynchronously linked to the primary database

# Backup
- Automatic backup to Amazon S3
- Manually taking a snapshot
- Backtracking (only for MySQL-compatible Aurora)

# Additional nodes
- You are not charged for data transfer when:
    - Any data transferred into your RDS database from the Internet
    - Transferred out to Amazon Cloudfront
    - Transferred out to EC2 instances in the same AZ
    - Transferred in or out between AZ for multi-AZ applications