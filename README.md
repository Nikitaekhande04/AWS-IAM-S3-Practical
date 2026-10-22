# AWS-IAM-S3-Practical
# AWS IAM & S3 Practical Examination

## Student Details
- **Name:** Nikita Ekhande
- **Batch:** MCA 24June
- **Topics:** AWS IAM and Amazon S3

## Practical Tasks Completed

### Task 1: Create IAM Users and Groups
Created two IAM users, `developer-user` and `tester-user`, and two groups, `Developers` and `Testers`. Added the users to their respective groups.

### Task 2: Attach IAM Policies
Attached `AmazonS3ReadOnlyAccess` to the Developers group and `AmazonS3FullAccess` to the Testers group.

**Expected Result:** Developers can read S3 resources permitted by the policy, while Testers have broader S3 permissions.

### Task 3: Create a Custom IAM Policy
Created a customer-managed policy named `CustomS3ReadPolicy` to allow listing the practical bucket and reading its objects without granting upload or delete permissions.

### Task 4: Create an IAM Role for EC2
Created an IAM role named `EC2S3ReadRole` with EC2 as the trusted service and read access to the specified S3 bucket.

### Task 5: Verify IAM Permissions
Tested S3 access using `developer-user`.

**Test Results:**
- Listing/accessing permitted bucket objects: Allowed
- Downloading `report.txt`: Allowed
- Uploading an object: Denied

*Note: Record the delete test result only if you actually tested it.*

### Task 6: Create and Secure an S3 Bucket
Created the S3 bucket `iam-policy-bucket-001`, enabled Block Public Access and default server-side encryption, and uploaded sample files.

### Task 7: Organize Objects and Enable Versioning
Created the `documents/`, `images/`, and `backups/` prefixes. Enabled bucket versioning and uploaded multiple versions of `report.txt`, then restored the earlier content as the current version.

### Task 8: Configure an S3 Bucket Policy
Configured a bucket policy to allow `developer-user` to read objects while keeping public access blocked. Tested object access using the intended IAM principal.

### Task 9: Configure a Lifecycle Rule
Created the enabled lifecycle rule `BackupTransitionRule` for objects under `backups/` to transition eligible objects to S3 Standard-IA after 30 days.

### Task 10: Configure Server Access Logging
Created the destination bucket `destination-bucket-logs-001`, enabled server access logging on the source bucket, and configured destination permissions for S3 log delivery.

*Note: Logging was enabled and permissions were configured. Successful log delivery should only be reported if a log object was observed in the destination bucket.*

### Task 11: Explain Encryption and Access Controls
Inspected the server-side encryption settings of an uploaded object and reviewed the differences between IAM policies and S3 bucket policies, along with the purpose of Block Public Access.

## Conclusion
Through this practical examination, I learned how to manage IAM users, groups, policies, and roles; secure S3 buckets; control object access; enable versioning and lifecycle rules; configure server access logging; and understand encryption and public access controls in AWS.
