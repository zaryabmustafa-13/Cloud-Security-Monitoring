AWS CloudTrail Monitoring & Audit Report

1. Objective

To implement AWS CloudTrail monitoring and audit management activities within the AWS cloud environment.

2. Initial Security Audit

The following activities were performed:

- Inspected CloudTrail Event History.
- Reviewed API activity and management events.
- Examined event timestamps, usernames, event sources and regions.
- Inspected individual event records and JSON details.
- Reviewed source IP addresses and event names.

3. CloudTrail Implementation

A new CloudTrail trail was successfully created.

Configuration                           Result
Trail name                              Cloud-Security-Audit-Trail
Logging status                          Enabled / Logging
S3 destination                          cloud-security-audit-primary-2026
Log folder prefix                       cloudtrail-logs
Management event monitoring             Configured during setup
Trail creation                          Successful

4. Evidence Collected

1. "01-CloudTrail-Event-History.png"
2. "02-CloudTrail-Event-Record.png"
3. "03-CloudTrail-Trail-Logging-Enabled.png"

5. Security Benefits

- Provides visibility into AWS account activity.
- Supports auditing of management API events.
- Helps investigate suspicious or unexpected activity.
- Stores audit logs in an S3 bucket for future examination.
- Supports security monitoring and incident investigation.

6. Conclusion

AWS CloudTrail was successfully configured, and its logging status was confirmed as Logging. The implementation provides an audit trail of AWS management activity and supports ongoing cloud security monitoring.

Multi-region configuration and final event-selector settings should be confirmed from the trail details before being reported as verified.