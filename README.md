Cloud Security Audit & Implementation
Internship Project
A practical cloud security audit and implementation project using Amazon Web Services (AWS). The project focuses on reviewing cloud security configurations, implementing security controls, monitoring account activity, and documenting findings with screenshots and reports.


Project Objectives
The main objectives of this project are:

- Audit Identity and Access Management (IAM) configurations.
- Implement secure backup practices and investigate multi-region redundancy.
- Configure AWS Web Application Firewall (WAF).
- Implement CloudTrail monitoring and logging.
- Collect evidence and document security findings.


Technologies and Services Used
Service                         Purpose
AWS IAM                         Identity and access management auditing
Amazon S3                       Secure storage and backup testing
AWS Backup                      Backup configuration assessment
AWS WAF                         Web application protection
Amazon CloudFront               Content delivery and WAF integration
AWS CloudTrail                  Account activity monitoring and auditing


Project Structure
Cloud-Security-Audit/
|
|__ README.md
|
|__01-IAM-Security-Audit/
|   |__ Evidence/
|   |__ AWS-IAM-Security-Audit-Report.md
|
|__ 02-Multi-Region-Backups/
|   |__ Evidence/
|   |__ Multi-Region-Backup-Audit-Report.md
|
|__ 03-Web-Application-Firewall/
|   |__ Evidence/
|   |__ AWS-WAF-Security-Audit-Report.md
|
|__ 04-CloudTrail-Monitoring/
    |__ Evidence/
    |__ AWS-CloudTrail-Monitoring-Report.md



1. Identity and Access Management (IAM) Audit
Activities Performed
- Inspected existing IAM roles.
- Reviewed AdministratorAccess permissions.
- Examined role trust relationships.
- Inspected AWS Organizations service-linked roles.
- Reviewed permissions and access configurations.
Security Importance
IAM auditing helps identify excessive permissions, understand role relationships, and improve access control within an AWS environment.
Deliverable: IAM Security Audit Report and supporting screenshots.



2. Multi-Region Backup and Storage Security
Activities Performed
- Inspected S3 buckets and AWS Backup configurations.
- Created an S3 bucket named "cloud-security-audit-primary-2026".
- Enabled S3 bucket versioning.
- Tested uploading multiple versions of an object.
- Demonstrated recovery of an earlier object version.
- Enabled all four S3 Block Public Access settings.
- Enabled default server-side encryption using SSE-S3.
- Reviewed backup plans and protected resources.
Important Finding
The primary S3 bucket was configured in the Sydney region ("ap-southeast-2").
Cross-region replication could not be completed because the required additional region was unavailable in the managed project environment.
Deliverable: Multi-Region Backup Audit Report and supporting screenshots.


3. Web Application Firewall (WAF) Implementation
Activities Performed
- Inspected the initial AWS WAF configuration.
- Reviewed existing Web ACLs, IP sets, rule groups, and regex pattern sets.
- Created a protection pack named "Cloud-Security-Audit-WAF".
- Added the AWS Managed Rules Common Rule Set (CRS).
- Created a CloudFront distribution named "Cloud-Security-Audit-Distribution".
- Configured Amazon S3 as the CloudFront origin.
- Enabled the existing WAF protection pack.
- Associated the protection pack with the CloudFront distribution.
- Verified the associated resource in AWS WAF.

Security Importance
AWS WAF helps inspect incoming web requests and protect applications against common web exploits and malicious traffic.
Implementation Result: The WAF protection pack was created and successfully associated with an enabled CloudFront distribution.
Deliverable: AWS WAF Security Audit Report and supporting screenshots.


4. CloudTrail Monitoring and Auditing
Activities Performed
- Inspected AWS CloudTrail Event History.
- Reviewed management events and API activity.
- Examined individual event records.
- Inspected event timestamps, usernames, event sources, regions, and source IP addresses.
- Reviewed event JSON details.
- Created a CloudTrail trail named "Cloud-Security-Audit-Trail".
- Configured the existing S3 bucket as the log destination.
- Used the "cloudtrail-logs" folder prefix.
- Confirmed that the trail status showed Logging.
Security Importance
AWS CloudTrail provides visibility into account activity and helps with security investigations, auditing, and monitoring changes made within an AWS environment.
Implementation Result: CloudTrail trail created successfully, with logging enabled.
Deliverable: AWS CloudTrail Monitoring Report and supporting screenshots.

Security Findings and Limitations
During the project, some limitations were encountered in the managed AWS environment:
- Cross-region backup configuration was restricted by regional availability.
- Some AWS service operations were restricted by project permissions.
- CloudFront pricing information displayed a missing-permissions message.
- AWS trial credits were available, but not all service charges were confirmed as credit-eligible.
These limitations were documented rather than reporting unsupported configurations as completed.

Project Outcomes
The project provided practical experience in:
- AWS identity and access management auditing.
- S3 storage security and object version recovery.
- Web application firewall configuration.
- CloudFront and WAF integration.
- CloudTrail management-event monitoring.
- Security evidence collection and technical reporting.
- Identifying and documenting cloud environment limitations.


Conclusion
This project demonstrates practical experience in auditing and implementing essential AWS cloud security controls.
Through IAM auditing, secure S3 storage configuration, WAF implementation, CloudFront integration, and CloudTrail monitoring, the project explores important aspects of cloud security, visibility, and operational protection.
All completed activities are supported by technical reports and evidence screenshots.
