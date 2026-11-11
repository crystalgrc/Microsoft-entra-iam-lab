# Microsoft Entra ID — Identity and Access Management Lab

## Project Overview
This hands-on lab demonstrates identity lifecycle management, role-based access control (RBAC), least privilege, and audit logging using Microsoft Entra ID Free.

## Lab Environment
- Microsoft Entra ID Free
- Microsoft Entra Admin Center
- Windows 11
- Microsoft Edge
- GitHub for documentation

## Lab Exercises Completed
1. Created a test employee account for Sarah Johnson.
2. Created an HR-Employees security group and assigned Sarah as a member.
3. Disabled Sarah's account and revoked sign-in sessions.
4. Reviewed audit logs to verify account changes.
5. Restored Sarah's account and confirmed group membership was retained.
6. Created a test IT helpdesk account for Michael Davis.
7. Assigned Michael the Helpdesk Administrator role.
8. Tested delegated password-reset permissions and confirmed Michael could not assign Global Administrator privileges.
9. Reset Sarah's password using Michael's account and verified the event in audit logs using the Global Administrator account.
10. Conducted a manual review of administrative role assignments.

## Security Concepts Demonstrated
- Identity lifecycle management
- User provisioning and deprovisioning
- Group-based access management
- Role-based access control (RBAC)
- Principle of least privilege
- Separation of duties
- Audit logging and verification
- Manual access reviews

## Key Findings
The Helpdesk Administrator account could perform a password reset for a standard user but could not assign Global Administrator privileges or access directory audit logs in the tested environment. Account disabling and restoration preserved security group membership.

## Future Lab Exercises
- Multifactor authentication and authentication methods
- Conditional Access concepts and licensing requirements
- PowerShell-based identity administration
- Microsoft 365 and Exchange Online administration

## Security Note
All employee identities are fictional. Sensitive tenant information, credentials, and unredacted audit records are excluded from this public repository.
