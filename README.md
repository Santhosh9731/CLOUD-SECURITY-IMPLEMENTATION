# CLOUD-SECURITY-IMPLEMENTATION

*COMPANY* : CODTECH IT SOLUTION

*NAME* : SANTHOSH GOVINDAN

*INTERN ID* : CT06DG1559

*DOMAIN* : CLOUD COMPUTING

*DURATION* : 6 WEEKS

*MENTOR* : NEELA SANTOSH

[cite_start]This report details the successful completion of a cloud security setup task for the CODTECH Cloud Internship, focusing on establishing fundamental security measures within an Amazon Web Services (AWS) environment[cite: 1, 2, 3]. [cite_start]The primary objective was to implement basic cloud security practices by configuring IAM policies, securing storage, and enabling data encryption on AWS[cite: 3, 4].

## Implementation Steps and Details:

### 1. IAM User and Policy Setup:
An integral part of this security setup involved the creation of a new IAM (Identity and Access Management) user in AWS. [cite_start]This user, named `codtech-user`, was granted precisely defined, limited access to an S3 bucket[cite: 6]. [cite_start]The permissions were meticulously configured to allow the user only to read and list files within the specified bucket[cite: 7]. [cite_start]Critically, the user was explicitly restricted from performing any delete or upload operations, which significantly enhances the security posture of the bucket by preventing unauthorized modifications[cite: 7, 8].

The policy applied to this IAM user is `ReadOnlyS3Policy`. This policy uses a JSON structure to define its permissions. The `Effect` is set to "Allow" for specific `Action`s. Specifically, the `Action`s permitted are `s3:ListBucket` and `s3:GetObject`. These actions are applied to the `Resource`s `arn:aws:s3:::my-bucket-name` (representing the bucket itself) and `arn:aws:s3:::my-bucket-name/*` (representing all objects within the bucket). In the actual implementation, the bucket name was `codtech-secure-bucket`.

### 2. Securing Storage:
[cite_start]For file storage, an S3 bucket was utilized[cite: 15]. [cite_start]A crucial security measure implemented was the complete disabling of public access for this S3 bucket[cite: 16]. [cite_start]This prevents any unauthorized external access to the files stored within, ensuring that data is not inadvertently exposed[cite: 16]. [cite_start]Consequently, access to the data within the bucket is strictly limited to the `codtech-user` IAM user, provided they possess the correct permissions defined earlier[cite: 17].

### 3. Data Encryption:
To ensure the confidentiality of the stored data, default encryption was enabled for the S3 bucket. The chosen encryption method was SSE-S3 (Server-Side Encryption with S3-managed keys). [cite_start]This configuration ensures that every file uploaded and stored in the bucket is automatically encrypted by AWS without requiring any additional manual steps from the user[cite: 20]. This "set-it-and-forget-it" encryption greatly simplifies data protection.

## Conclusion:
[cite_start]By meticulously implementing a limited IAM user with granular permissions, disabling public access to the S3 bucket, and activating default server-side encryption, the cloud storage on AWS has been effectively secured[cite: 22, 23]. [cite_start]These steps collectively align with and demonstrate adherence to good cloud security practices, ensuring the integrity and confidentiality of data stored in the cloud environment[cite: 23].

## OUTPUT 

