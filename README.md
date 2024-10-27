
# Flaws Cloud Capture the Flag (CTF) Challenge

## Author

- **Sherine Paul Raj**
- UID: 119362921

## Challenge Overview

This report documents the solutions to the Flaws Cloud Capture the Flag (CTF) challenge. The project demonstrates how to exploit various AWS configurations to access secret files and navigate through different challenge levels using AWS S3, CLI, and other cloud tools.

## Table of Contents

1. [Challenge 1: URL for the Secret File](#challenge-1-url-for-the-secret-file)
2. [Challenge 2: Accessing the Secret File Using Amazon CLI](#challenge-2-accessing-the-secret-file-using-amazon-cli)
3. [Challenge 3: Listing Files in the S3 Bucket](#challenge-3-listing-files-in-the-s3-bucket)
4. [Key Learnings](#key-learnings)
5. [Conclusion](#conclusion)

## Challenge 1: URL for the Secret File

The URL for the secret file discovered during the first challenge is:
- **URL**: [Secret File](https://flaws.cloud.s3.amazonaws.com/secret-dd02c7c.html)

## Challenge 2: Accessing the Secret File Using Amazon CLI

Using the Amazon CLI, the URL for the secret file was:
- **URL**: [Level 2 Secret File](http://level2-c8b217a33fcf1f839f6f1f73a00a9ae7.flaws.cloud/secret-e4443fc.html)

Command executed to list and access the file:
```bash
aws s3 ls s3://<bucket-name>
```

## Challenge 3: Listing Files in the S3 Bucket

Through the AWS S3 CLI, it was possible to list the files within the S3 bucket. This process helped in identifying the structure of the data and understanding how to navigate to other secret files.

Example command:
```bash
aws s3 ls s3://<bucket-name> --recursive
```

## Key Learnings

- **Understanding AWS S3 Permissions**: The challenges highlighted the importance of configuring S3 permissions correctly to prevent unauthorized access.
- **Effective Use of AWS CLI**: Utilizing AWS CLI commands to interact with cloud resources efficiently.
- **Security Best Practices**: Learning about potential vulnerabilities in cloud configurations and how to avoid them.

## Conclusion

The Flaws Cloud CTF challenge served as an insightful project to understand how misconfigured AWS services can lead to security risks. Through practical hands-on experience, the project emphasized the importance of securing cloud resources and applying best practices in AWS configurations.
