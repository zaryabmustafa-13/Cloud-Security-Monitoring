AWS WAF Security Audit and Implementation Report

1. Project Overview
Project: Cloud Security Audit and Implementation
Service: Amazon Web Services (AWS)
Component: Web Application Firewall (WAF)
Region: Sydney ("ap-southeast-2")
Protection Pack: "Cloud-Security-Audit-WAF"
CloudFront Distribution: "Cloud-Security-Audit-Distribution"

2. Objective
The objective of this task was to audit the existing AWS WAF configuration and implement web application protection using AWS Managed Rules and Amazon CloudFront.
The implementation aimed to introduce an additional security layer for inspecting incoming web requests and protecting web applications against common threats.

3. Initial Security Audit
During the initial inspection of AWS WAF, the following configuration was observed:
Security Component| Initial Status
Web ACLs| 0
IP Sets| 0
Rule Groups| 0
Regex Pattern Sets| 0
The initial audit indicated that no Web ACLs or custom WAF security resources were configured in the inspected environment.

4. Implementation
4.1 Creation of WAF Protection Pack
A protection pack was created with the following configuration:
- Name: "Cloud-Security-Audit-WAF"
- Description: AWS WAF implementation for cloud security internship
- Configuration: Build your own protection pack
- Application Category: Other
- Application Focus: Web

4.2 AWS Managed Rules Configuration
The AWS Managed Rules Common Rule Set (CRS) was added to the protection pack.
Configuration details:
- Rule Group: AWS Managed Rules Common Rule Set
- Capacity: 700 WCU
- Inspection: Request inspection
- Rule Actions: Default AWS managed rule actions retained
- Override All Rules: Not enabled
The Common Rule Set provides predefined protections against common web application vulnerabilities and suspicious request patterns.

4.3 CloudFront Distribution
A CloudFront distribution was created with the following details:
- Distribution Name: "Cloud-Security-Audit-Distribution"
- Description: CloudFront distribution for AWS WAF internship testing
- Distribution Type: Single website configuration
- Origin: Existing S3 bucket "cloud-security-audit-primary-2026"
- Domain Configuration: Route 53 managed domain skipped

4.4 WAF Integration
During the CloudFront security configuration, the previously created WAF protection pack was enabled.
The association was subsequently verified through the WAF protection pack's resource management section.
The CloudFront distribution also displayed the Web Application Firewall as enabled under its Security section.

5. Verification Results
The following implementation results were observed:
Verification Item| Result
WAF protection pack created| Successful
Common Rule Set added| Successful
CloudFront distribution created| Successful
WAF enabled for CloudFront| Confirmed
WAF resource association| Confirmed
CloudFront distribution status| Enabled
Live attack-blocking test| Not performed

6. Security Considerations and Limitations

- The WAF protection pack was successfully associated with the CloudFront distribution.
- No custom IP sets, regex pattern sets, or custom rule groups were created.
- Live malicious traffic testing was not performed; therefore, actual attack-blocking effectiveness was not independently validated.
- The initial resource configuration was recorded before implementation and retained as audit evidence.
- The console displayed an estimated monthly WAF cost of approximately $12 per 10 million requests during configuration. This is a usage-based estimate, not a one-time charge. Credit eligibility and final billing were not independently verified.
- The CloudFront pricing section displayed a missing-permissions notice in the project environment.

7. Evidence Collected

The following screenshots document the audit and implementation:

1. "01-WAF-Web-ACLs-Overview.png"
2. "02-WAF-Rule-Groups.png"
3. "03-WAF-Regex-Pattern-Sets.png"
4. "04-WAF-IP-Sets.png"
5. "05-WAF-No-Associated-Resources.png" (initial state, if captured)
6. "06-CloudFront-WAF-Enabled.png"
7. "07-CloudFront-Distribution-Details.png"
8. "08-WAF-CloudFront-Resource-Association.png"
9. "09-CloudFront-Distribution-Enabled.png"

8. Conclusion
The AWS WAF audit and implementation established a web application protection configuration using the AWS Managed Rules Common Rule Set and Amazon CloudFront.
The protection pack was created, enabled for the CloudFront distribution, and its resource association was verified.
This practical implementation demonstrated how managed security rules and content delivery infrastructure can be integrated to strengthen web application security.