# <ins> Assignment-2-12: Assignment 2-12 Function as a Service <ins>

## Given a Lambda function that is triggered upon the creation of files in an S3 bucket, answer the following:

### 1. What is the purpose of the execution role on the Lambda function?
- Defines the permissions that the function has when it is executed.
- It is an AWS Identity and Access Management (IAM) role that grants the Lambda function the necessary permissions to interact with the S3 bucket
- The execution role ensures that the Lambda function operates securely and only performs actions it is explicitly allowed to do
- source: https://docs.aws.amazon.com/lambda/latest/dg/lambda-intro-execution-role.html

### 2. What is the purpose of the resource-based policy on the Lambda function?
- The resource-based policy on a Lambda function controls which AWS services or accounts are allowed to invoke the function.
- In this case, the S3 bucket needs permission to trigger the Lambda function when a file is created.
- The resource-based policy allows the S3 bucket to invoke the Lambda function, enabling the event-driven architecture where the function is automatically triggered by S3 events.
- source: https://docs.aws.amazon.com/lambda/latest/dg/access-control-resource-based.html

### 3. If the function is needed to upload a file into an S3 bucket, describe (i.e no need for the actual policies)

### What is the needed update on the execution role?
- To allow the Lambda function to upload files to an S3 bucket, the execution role must be updated to include the necessary permissions.
- Specifically, the role needs the s3:PutObject permission for the target S3 bucket.

### What is the new resource-based policy that needs to be added (if any)?

