# Features
- Pay for what you use (On-demand)
- Spend less by reserving instances (Reserve)
- Meet compliance rules using reliable dedicated cloud computing resources (dedicated)
- Ephemeral (= temporary): local storage attached to EC2 instances
    - Physically attached (= no way to detach it from any EC2 instance)
    - All data is lost if it is stopped or terminated
    - Data is intact if it is just rebooted.
# Amazon Machine Images (AMIs)
- Template of EC2 instances with some configuration
- A pre-defined AMI, community AMI and custom AMI to launch a new instance

# Pricing / Classes / Tenancy
## Purchasing options
- On-demand: Flat rate, no commitment
- On-demand CAPACITY reservations (immediately available instances that meet your needs / specification)
- Reserved: All upfront / partial upfront / no upfront (high to low discounted rate)
- Scheduled: You would be still charged even if you don't use it
- Spot: It can be terminated in the middle of process anytime, if your bid price is lower than the spot price

## Classes
- General
- Micro
- Memory optimized
- Compute
- GPU
- FPGA (ex. financial computing)
- Storage

## Tenancy
- Shared tenancy: Any random host shared by multiple isolated customers
- Dedicated instances: Instances for a single customer (who needs to meet compliance / security requirements)
- Dedicated hosts: Additional visibility and control on a physical host - good for using your software license

# Related Products

## Elastic Load Balancing (ELB)
## Auto Scaling Group
