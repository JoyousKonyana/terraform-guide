## Create Remote state

### Advantages of Remote State (AWS S3):
- **Collaboration**: Supports team collaboration by providing a centralized location for state files.
- **Locking Mechanisms**: Prevents conflicts during concurrent operations.
- **Security**: Uses AWS IAM roles and policies for access control.
- **Version Controlled** : Take advantage of S3 versioning
- **Durability and Availability**: AWS S3 ensures automatic durability and availability for state files.

 **AWS S3 Bucket**  this will be used to store the state file remotely.

 **AWS Dynamodb to store the lock files**  this will be used to lock files so that only one user can make changes at a time.

 ## AWS S3 Bucket

  **Region**  N-viginia
  **Block all public access:**  True
  **Enable bucket versioning:** True
  **Enable bucket versioning:** True
  **Enable default encryption:** True

  **S3 Bucket policy:** 

  **Syntax**: 

```hcl
{
    "Version": "2012-10-17",
    "Id": "Policy1680820022117",
    "Statement": [
        {
            "Sid": "Stmt1680819929502",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::<account>:user/USER"
            },
            "Action": [
                "s3:DeleteObject",
                "s3:GetObject",
                "s3:ListBucket",
                "s3:PutObject"
            ],
            "Resource": [
                "arn:aws:s3:::S3-BUCKET-NAME",
                "arn:aws:s3:::S3-BUCKET-NAME/path-to-state-file"
            ]
        },
        {
            "Sid": "Stmt1680819959950",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:DeleteBucket",
            "Resource": "arn:aws:s3:::S3-BUCKET-NAME"
        }
    ]
}
```

## AWS DynamoDB table
  **Partition key:**  LockID
  **Read/Write capacity settings:** On-demand
  **Deletion protection:**  True

  ## Declare the backend

  **Syntax**: 

```hcl
terraform {
  backend "s3" {
    bucket         = "s3-bucket-name"
    key            = "path-to-state"
    region         = "region"
    encrypt        = true
    dynamodb_table = "your-dynamodb-table"
  }
}
```