# Features
- A user is charged for the total amount of throughput + total amount of storage space in use
- Data is replicated automatically across three different AZ within a region

# Details
- Rules:
    - Each record in a table do not need to have the same attributes or the same number of attributes (except primary key)
    - Each query can only use one index.
        - Maching on two different columns, for example, needs creating another index
    - You need to specify the exact index used for the query
- Seconday indexes: It allows you to perform queries on attributes that are not a primary key
    - Type 1: Global indexes - you can query across the entire table
    - Type 2: Local seconday indexes - you are able to find data in a single partition key

# DynamoDB Accelerator (DAX)
- With DAX and DynamoDB, you can enjoy extremely enhanced performance of DynamoDB by mitigating the problem of eventual consistency
- When it comes to its architecture, DAX that uses in-memory cache is separated from DynamoDB and resides in your VPC (On the other hand, DynamoDB is outside of your VPC)
- When DAX is being configured, we need to select a subnet group which allows DAX to deploy a node in each of subnets of the subnet group - so that other nodes except the primary one become read replicas. When they receive requests, traffic is load balanced and distributed across all nodes in the cluster.