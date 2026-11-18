
# Microsoft Entra ID — Identity and Access Management Lab

## Project Overview

This hands-on cybersecurity lab demonstrates identity lifecycle management, user provisioning and offboarding, role-based access control (RBAC), least privilege, and audit logging using Microsoft Entra ID.

The project simulates real-world identity administration scenarios for a fictional organization, Contoso Technologies, and documents administrative procedures, security controls, verification results, and supporting evidence.

## Lab Environment

- Microsoft Entra ID Free
- Microsoft Entra Admin Center
- Windows 11
- Microsoft Edge
- GitHub for technical documentation and evidence

## Lab Portfolio

| Lab | Description | Status |
|---|---|---|
| [Lab 01: User Provisioning and Group Management](labs/01-user-provisioning.md) | User account creation, security groups, membership assignment, and audit verification | Completed |
| [Lab 02: Employee Offboarding and Audit Logging](labs/02-employee-offboarding.md) | Account disablement, session revocation, group membership removal, and audit verification | Completed |
| [Lab 03: RBAC and Least Privilege](labs/03-rbac-least-privilege.md) | Delegated administration, password resets, privilege restrictions, and access reviews | Completed |

## Completed Lab Highlights

### Lab 01 — User Provisioning and Group Management

- Created a fictional employee account for Sarah Johnson.
- Created the HR-Employees security group.
- Assigned Sarah to the departmental security group.
- Verified user account properties and group membership.
- Reviewed user creation and group membership audit events.
- Captured and documented supporting evidence.

### Lab 02 — Employee Offboarding and Audit Logging

- Verified the employee's initial account status and group membership.
- Disabled Sarah Johnson's account.
- Revoked sign-in sessions.
- Removed membership in HR-Employees.
- Verified account disablement and group removal through audit logs.
- Investigated the StsRefreshTokensValidFrom modified property to verify session revocation.
- Retained the disabled identity record for administrative and audit purposes.

[View Lab 02 Evidence](evidence/lab-02-employee-offboarding/)

### Lab 03 — RBAC and Least Privilege

- Created a fictional IT Helpdesk Technician account for Michael Davis.
- Assigned and verified the Helpdesk Administrator role.
- Tested delegated password-reset permissions for a standard user.
- Confirmed that Global Administrator role assignment was restricted.
- Verified that directory audit logs were inaccessible to the Helpdesk Administrator in the tested configuration.
- Reviewed password-reset audit logs using the Global Administrator account.
- Conducted a manual administrative access review.
- Captured four screenshots demonstrating role assignments, privilege restrictions, and authorized password-reset access.

[View Lab 03 Evidence](https://github.com/crystalgrc/Microsoft-entra-iam-lab/tree/main/evidence/lab-03-rbac-least-privilege)

## Security Concepts Demonstrated

- Identity lifecycle management
- User provisioning and deprovisioning
- Group-based access management
- Account disablement and session revocation
- Role-based access control (RBAC)
- Principle of least privilege
- Separation of duties
- Audit logging and verification
- Manual access reviews

## Key Findings

- Security groups simplify access management by allowing permissions to be managed collectively.
- Disabling an employee account prevents new sign-ins but does not necessarily terminate all previously issued access tokens immediately.
- Session revocation can be verified by examining the StsRefreshTokensValidFrom property in directory audit logs.
- Removing security group membership eliminates access associated with that membership.
- Delegated administrative roles support least privilege by limiting administrative capabilities to authorized tasks.
- In the tested environment, the Helpdesk Administrator could reset a standard user's password but could not assign Global Administrator privileges or access directory audit logs.

## Scope and Limitations

This project uses Microsoft Entra ID Free and fictional employee identities.

No production applications, employee data, or organizational resources are involved. The labs demonstrate directory administration, security configuration, and audit verification rather than production application access.

Premium identity governance and Conditional Access capabilities are outside the current lab scope.

## Future Lab Exercises

- Multifactor authentication and authentication methods
- Conditional Access concepts and licensing requirements
- PowerShell-based identity administration
- Microsoft 365 and Exchange Online administration
- Windows Server and Active Directory administration
- Hybrid identity concepts

## Security Note

All employee identities are fictional. Sensitive tenant information, credentials, personal account information, and unredacted audit records are excluded from this public repository.
