Multi-Region Backup Security Audit and Implementation Report

1. Project Overview
Project: Cloud Security Audit and Implementation
Service: Amazon Web Services (AWS)
Component: S3 Storage Security and Multi-Region Backup Audit
Primary Region: Sydney ("ap-southeast-2")
Primary S3 Bucket: "cloud-security-audit-primary-2026"

2. Objective
The objective of this task was to examine AWS backup configurations, assess existing backup resources, and implement basic S3 data protection measures.

The audit focused on:
- S3 bucket security
- Object versioning
- Data recovery
- Public access restrictions
- Default encryption
- AWS Backup resources and plans
- Multi-region backup availability

3. Initial Backup Audit
During the initial inspection, the following conditions were observed in the Sydney region:
Component| Initial Status
S3 Buckets| 0
AWS Backup Protected Resources| 0
AWS Backup Plans| 0
The initial inspection showed that no S3 buckets, protected resources, or backup plans were present in the inspected environment.

4. S3 Bucket Implementation
A primary S3 bucket was created in the Sydney region.
Bucket Name: "cloud-security-audit-primary-2026"
The following security configurations were applied:
Configuration| Setting
Object Ownership| Bucket owner enforced
ACLs| Disabled
Block Public Access| All four settings enabled
Bucket Versioning| Enabled
Default Encryption| SSE-S3
Object Lock| Disabled

4.1 Versioning Configuration
Bucket versioning was enabled to preserve multiple versions of stored objects.
To test the configuration:
1. A test file named "backup-test.txt" was uploaded.
2. The file content was modified.
3. The modified file was uploaded again.
4. The available object versions were inspected.
5. The earlier version was recovered and downloaded.
The test confirmed that S3 versioning was functioning and that an earlier version of the object could be retrieved.

4.2 Public Access Protection
All four S3 Block Public Access settings were enabled.
This configuration helps prevent accidental public exposure of bucket data.

4.3 Default Encryption
Default server-side encryption using SSE-S3 was configured to provide encryption for stored objects.

5. AWS Backup Inspection
The AWS Backup service was inspected to evaluate the existing backup infrastructure.
The initial inspection showed:
- No protected resources.
- No existing backup plans.
The backup vault creation interface was also examined. However, a complete AWS Backup vault and backup plan configuration was not established.
Therefore, no scheduled AWS Backup job or protected-resource backup is claimed as completed in this implementation.

6. Multi-Region Backup Assessment
The primary S3 bucket was created in the Sydney region ("ap-southeast-2").
The Mumbai region ("ap-south-1") was initially inspected but later became unavailable in the managed project environment. The project environment did not allow the region to be changed.

As a result:
- A second regional backup bucket was not configured.
- Cross-region replication was not established.
- Multi-region backup redundancy could not be verified.
This is recorded as an environment limitation rather than a completed implementation.

7. Verification Results
Security Control| Result
Primary S3 bucket created| Successful
Bucket versioning| Enabled
Multiple object versions| Verified
Previous version recovery| Successfully demonstrated
Block Public Access| All four settings enabled
Default SSE-S3 encryption| Configured
AWS Backup plans| None configured
Protected resources| None confirmed
Cross-region replication| Not configured

8. Evidence Collected
The following screenshots document the audit and implementation:
1. "01-S3-Buckets-Overview.png"
2. "02-AWS-Backup-Protected-Resources.png"
3. "03-AWS-Backup-Plans-Overview.png"
4. "04-S3-Versioning-Enabled.png"
5. "05-S3-Two-Object-Versions.png"
6. "06-S3-Old-Version-Recovery.png"
7. "07-S3-Block-Public-Access-Settings.png"
8. "08-S3-Default-Encryption.png"

9. Conclusion
The backup security audit resulted in the creation of a secured S3 bucket in the Sydney region.
Versioning was enabled and tested through multiple object uploads and recovery of an earlier version. Public access restrictions and default encryption were also configured.
However, cross-region replication and scheduled AWS Backup protection were not completed because of limitations in the managed project environment.
The implementation demonstrates important S3 data protection and recovery capabilities while identifying the remaining requirements for a complete multi-region backup strategy.