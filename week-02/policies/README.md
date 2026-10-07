# Week 2 IAM Policies

## S3UploaderOnly-AdamSadowsky

This policy allows the `s3-test-user` IAM user to upload and download objects in the `my-training-bucket-AdamSadowsky` S3 bucket.

Allowed actions:
- `s3:PutObject`
- `s3:GetObject`

The resource is scoped to:

`arn:aws:s3:::my-training-bucket-AdamSadowsky/*`

The `/*` limits the permissions to objects inside that specific bucket. The policy does not allow listing all S3 buckets, deleting objects, creating buckets, or accessing other buckets. This follows the principle of least privilege by granting only the permissions needed for the lab.