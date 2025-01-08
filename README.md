**1.AWS VPC with Public and Private Subnets in Production**

VPC Design and Implementation: Designed a VPC with public subnets (NAT gateways and load balancers) and private subnets (servers managed by Auto Scaling) across two Availability Zones.

Traffic Management: Set up a load balancer to distribute incoming traffic to servers in private subnets; enabled internet access for private subnets via NAT gateways.

Performance and Security: Managed VPC components ensuring high availability, compliance with AWS best practices, and enhanced security measures.

**2.AWS Cloud Cost Optimization**

Identifying Stale EBS Snapshots:
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if it exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
