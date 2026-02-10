# Encrypt-S3-bucket-EBS-Volume-and-AMI-using-AWS-KMS
AWS-kms-encryption-lab- A hands-on AWS security lab demonstrating how to encrypt Amazon S3 buckets, EBS volumes, and AMIs using AWS Key Management Service (KMS), with a focus on key management, access control, and encryption best practices.
# Lab: Encrypt S3 Buckets, EBS Volumes, and AMIs Using AWS KMS

## Introduction
Encryption is a foundational security control for protecting data at rest in the cloud. AWS Key Management Service (KMS) is a fully managed encryption service that allows you to create, manage, and control cryptographic keys used to secure your data across AWS services.

In this lab, you will use AWS KMS to encrypt Amazon S3 buckets, Amazon EBS volumes, and Amazon Machine Images (AMIs). You will also learn how AWS services integrate with KMS to provide centralized key management and strong access control.

---

## What is AWS KMS?
AWS Key Management Service (KMS) is a managed service that enables you to create and control encryption keys used to protect data and workloads within AWS. It simplifies key management while providing strong security controls, auditing, and compliance support.

AWS KMS is a critical service for securing sensitive data and meeting encryption and regulatory requirements without the complexity of building and managing your own key management infrastructure.

---

## Key Features of AWS KMS

### Key Creation and Management
- Create customer-managed keys (CMKs)
- Enable automatic key rotation
- Manage key lifecycle and permissions

### Integration with AWS Services
AWS KMS integrates seamlessly with:
- Amazon S3
- Amazon EBS
- Amazon EC2 and AMIs
- Amazon RDS
- Many other AWS services

### Envelope Encryption
AWS KMS uses envelope encryption:
- Data is encrypted using a data key
- The data key is encrypted with a KMS-managed key
- Improves security and performance

### Key Policies and Access Control
- Define fine-grained access using key policies and IAM
- Restrict who can encrypt, decrypt, and manage keys

### Logging and Monitoring
- Track key usage with AWS CloudTrail
- Monitor activity and alerts using Amazon CloudWatch

### Custom Key Store
- Use AWS CloudHSM-backed custom key stores
- Useful for strict compliance and regulatory requirements

### Regional Service
- KMS keys are region-specific
- Helps meet data residency and compliance requirements

---

## Lab Objectives
By completing this lab, you will learn how to:

- Create and manage KMS customer-managed keys
- Encrypt an Amazon S3 bucket using AWS KMS
- Encrypt Amazon EBS volumes using KMS keys
- Create encrypted AMIs
- Enable and understand automatic key rotation
- Review encryption and key usage

---

## Prerequisites
- An AWS account
- IAM permissions for:
  - AWS KMS
  - Amazon S3
  - Amazon EC2 / EBS
- Basic understanding of:
  - AWS EC2 and S3
  - Encryption concepts

---

## Lab Guide
Follow the step-by-step instructions in the `lab-guide/` directory:

1. **Prerequisites and IAM Setup**
2. **Create a KMS Customer-Managed Key**
3. **Encrypt an S3 Bucket**
4. **Encrypt an EBS Volume**
5. **Create an Encrypted AMI**
6. **Enable Automatic Key Rotation**
7. **Clean Up Resources**

---

## Did You Know?
**Key Rotation**  
AWS KMS supports automatic key rotation, which enhances security by periodically changing encryption keys without impacting encrypted data.

---

## Cost Considerations
- AWS KMS charges per key and per API request
- Encrypted EBS snapshots and AMIs may incur storage costs
- Always clean up resources after completing the lab

---

## Cleanup
To avoid unnecessary charges:
- Disable or schedule deletion of KMS keys
- Delete test S3 buckets
- Remove EC2 instances, EBS volumes, and AMIs

---

## License
This project is licensed under the MIT License.
