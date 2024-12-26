## AWS IAM (Identity and Access Management)
AWS Identity and Access Management (IAM) is a web service that enables secure access control for AWS resources. It allows you to manage permissions and authentication for users, groups, roles, and applications interacting with AWS services.

## Key Features of IAM
- **Granular Access Control**: Define fine-grained permissions to allow or deny specific actions on AWS resources.
  
- **Centralized Management**: Manage access for multiple AWS services from a single place.
  
- **Secure Credentials**: Use temporary credentials (roles) to reduce security risks.
  
- **Federated Access**: Integrate with external identity providers for user authentication.


# **AWS IAM Concepts for S3**

## **1. Users**
- Represents a person or service requiring access to AWS.
- Each user has unique credentials (Access Key ID, Secret Access Key).
- Permissions are assigned via policies.

## **2. User Groups**
- A collection of IAM users with shared permissions.
- Policies applied to a group apply to all its users.
- Simplifies access management.

## **3. Roles**
- Permissions temporarily assumed by trusted entities (users, services, or applications).
- Allows secure access without sharing credentials.
- Commonly used for AWS services like EC2 or Lambda.

## **4. Policies**
- JSON documents defining permissions for users, groups, or roles.
- Types:
  - **AWS Managed Policies**: Predefined by AWS.
  - **Customer Managed Policies**: Created by the user.
  - **Inline Policies**: Attached directly to an entity.
- Example Policy:
  ```json
  {
    "Version": "2012-10-17",
    "Statement": [
      {
        "Effect": "Allow",
        "Action": ["s3:ListBucket", "s3:GetObject"],
        "Resource": ["arn:aws:s3:::example-bucket", "arn:aws:s3:::example-bucket/*"]
      }
    ]
  }
