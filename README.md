**1.AWS VPC with Public and Private Subnets in Production**

VPC Design and Implementation: Designed a VPC with public subnets (NAT gateways and load balancers) and private subnets (servers managed by Auto Scaling) across two Availability Zones.

Traffic Management: We set up a load balancer to distribute incoming traffic to servers in private subnets and enabled internet access for private subnets via NAT gateways.

Performance and Security: Managed VPC components ensuring high availability, compliance with AWS best practices, and enhanced security measures.

**2.AWS Cloud Cost Optimization**

Identifying Stale EBS Snapshots:
In this example, we'll create a Lambda function that identifies EBS snapshots no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if it exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.



**2.AWS End-to-End CI-CD**

Description:

This project sets up a Continuous Integration (CI) pipeline using AWS to automate the build and deployment of a Python application. It involves creating a GitHub repository, configuring AWS CodePipeline to automate the flow from code changes to deployment, and using AWS CodeBuild to handle the build and testing process. The goal is to streamline the development workflow and ensure faster, more reliable delivery of the application.
