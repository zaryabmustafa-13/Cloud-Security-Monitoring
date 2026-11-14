AWS CLOUD SECURITY AUDIT REPORT

Identity and Access Management (IAM)

Internship Task: Cloud Security Audit
Platform: Amazon Web Services (AWS)
Service: Identity and Access Management (IAM)
Audit Type: IAM Roles and Permissions Review


1. Objective

The objective of this audit was to review AWS IAM roles, their attached permissions policies, trusted entities, and recent activity.

The purpose was to identify potentially excessive permissions, examine access relationships, and evaluate the security of role-based access management.

2. IAM Roles Overview

The IAM Roles dashboard was inspected to identify existing roles and review their activity.

The inspection included:

- Role names
- Attached permissions policies
- Policy types
- Trusted entities
- Last activity information

3. Detailed IAM Audit Findings

Finding 1: AdministratorAccess Role

Attached Policy: AdministratorAccess
Policy Type: AWS Managed
Trusted Service: "account.amazonaws.com"

Observation:

The AdministratorAccess policy provides broad administrative permissions across AWS services and resources.

Security Risk:

If this role is accessible to an unauthorized identity, it could result in extensive control over AWS resources.

Recommendation:

- Review which identities can assume this role.
- Restrict administrative access to authorized identities.
- Apply the principle of least privilege.
- Monitor administrative activities through AWS CloudTrail.

Assessment: High-privilege role requiring further review.

Finding 2: AWS Organizations Service Role

Role Name: AWSServiceRoleForOrganizations
Attached Policy: AWSOrganizationsServiceRolePolicy
Policy Type: AWS Managed
Trusted Service: "organizations.amazonaws.com"

Observation:

This is a service-linked role that allows AWS Organizations to perform its required operations.

Security Assessment:

The attached AWS-managed policy and trusted service are consistent with the role's intended purpose.

Recommendation:

Retain the role when required by AWS Organizations and periodically review its configuration.

Assessment: Expected service-linked role.

Finding 3: AWS Managed Account Management Access Role

Attached Policy: AWS Managed Account Management Access
Policy Type: AWS Managed

Observation:

This role is associated with AWS account management functionality.

Recommendation:

Verify its permissions and trusted entities to ensure access is limited to the intended account management operations.

Finding 4: AWS Managed Advanced Feature Activation Role

Attached Policy: AWS Managed Advanced Feature Activation Access
Policy Type: AWS Managed

Observation:

This role is associated with advanced feature activation functionality.

Recommendation:

Review its trust relationship and permission scope to ensure that only authorized AWS services or identities can use it.

Finding 5: AWS User Notification Service Role

Role Name: AWSServiceRoleForUserNotifications
Attached Policy: AWS User Notification Service Linked Role Policy
Policy Type: AWS Managed

Observation:

This service-linked role supports AWS User Notifications.

Recommendation:

Verify that the role is used by the intended AWS service and that its permissions remain appropriate.

Finding 6: AWS Budgets Spend Limit Member Role

Role Name: AWSServiceRoleForBudgetsSpendLimit
Attached Policy: AWS Budgets Spend Limit Member Role Policy
Policy Type: AWS Managed

Observation:

This role supports AWS Budgets spend-limit functionality.

Recommendation:

Review its permissions and trust relationship to ensure that budget-related operations are appropriately restricted.

Finding 7: AWS IAM Role Manager Service Role

Role Name: AWSServiceRoleForIAMRoleManager
Attached Policy: AWS IAM Role Manager Service Role Policy
Policy Type: AWS Managed

Observation:

This role is associated with IAM role management functionality.

Recommendation:

Review its permissions carefully because role-management capabilities can affect account security and access control.


Finding 8: AWS Support Service Role

Role Name: AWSServiceRoleForSupport
Attached Policy: AWS Support Service Role Policy
Policy Type: AWS Managed

Observation:

This role is associated with AWS Support operations.

Recommendation:

Verify that it is used for authorized support-related operations and that its trust relationship is appropriate.

Finding 9: AWS Trusted Advisor Service Role

Role Name: AWSServiceRoleForTrustedAdvisor
Attached Policy: AWS Trusted Advisor Service Role Policy
Policy Type: AWS Managed

Observation:

This role supports AWS Trusted Advisor operations.

Recommendation:

Review its permissions and trusted entities to ensure that access is limited to the required service operations.

4. IAM Activity Review

During the IAM Roles inspection, the following observations were recorded:

- Two roles showed recent activity of approximately 6 minutes ago and  3 hours ago.
- Other roles displayed no last activity.

Security Consideration:

Roles without recorded recent activity should be reviewed to determine whether they are still required.

The absence of recent activity does not necessarily mean that a role is unused or unnecessary. Some AWS service-linked roles are activated only when particular services perform specific operations.

Recommendation:

Review role usage and associated services before making any changes.

5. Security Recommendations

The following security practices are recommended:

1. Follow the principle of least privilege.
2. Restrict administrative access to authorized identities.
3. Regularly review IAM roles and attached policies.
4. Verify trusted entities and trust relationships.
5. Monitor account activities through AWS CloudTrail.
6. Investigate roles with no recorded recent activity.
7. Avoid unnecessary permission changes to AWS service-linked roles.
8. Conduct periodic IAM security reviews.

6. Evidence Collected

Screenshots were captured to document the following audit evidence:

- IAM Roles overview.
- AdministratorAccess permissions policy.
- Administrator role trust relationship.
- AWS Organizations permissions policy.
- AWS Organizations trust relationship.

These screenshots support the observations documented in this report.

7. Audit Limitations
This audit was an initial, read-only inspection.
- Not every role's complete permission set was examined.
- The permissions and trust relationships of all roles were not independently verified.
- Role usage and necessity require further investigation.
- No IAM roles or policies were modified during the inspection.

8. Conclusion

The IAM security audit provided an initial overview of AWS role-based access management.

The review identified a role with broad administrative permissions that requires particular attention. Several AWS-managed service-linked roles were also identified, supporting different AWS service operations.

Regular permission reviews, trusted-entity verification, least-privilege access, and activity monitoring are recommended to strengthen the security of the AWS environment.

Audit Status: Initial IAM inspection completed. Further verification recommended.