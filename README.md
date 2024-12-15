# Lambda-AWS-Proj

Identifying Unused EBS Snapshots
In this example, we will create a Lambda function designed to identify EBS snapshots that are no longer linked to any active EC2 instance and delete them to reduce storage costs.

Description:
The Lambda function retrieves all EBS snapshots owned by the same account ("self") and fetches a list of active EC2 instances, including both running and stopped instances. For each snapshot, it checks if the associated volume (if present) is still linked to any active EC2 instance. If the function detects an unused snapshot, it deletes it, helping to optimize storage costs.
