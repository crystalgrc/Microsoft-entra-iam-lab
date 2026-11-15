# Lab 01: User Provisioning and Group Management

## Objective
Demonstrate the ability to provision user accounts, create security groups, assign group membership, and verify access configurations using Microsoft Entra ID.

## Lab Environment
- Microsoft Entra ID Free
- Microsoft Entra Admin Center
- Windows 11
- Microsoft Edge

## Scenario
A fictional organization, Contoso Technologies, has hired Sarah Johnson as a Human Resources employee. The IT administrator must create her account and assign her to the appropriate departmental security group.

## Procedure

### 1. User Account Creation
1. Navigated to Microsoft Entra ID > Users > All users.
2. Selected New user > Create new user.
3. Entered the fictional employee's name and user principal name.
4. Configured the account as enabled and used an auto-generated initial password.
5. Created the account and verified it appeared in the directory.

### 2. Security Group Creation
1. Navigated to Microsoft Entra ID > Groups > All groups.
2. Created a security group named HR-Employees.
3. Selected Assigned membership.
4. Added Sarah Johnson as a group member.
5. Verified her membership in the group.

### 3. Audit Log Verification
1. Navigated to Microsoft Entra ID > Monitoring & health > Audit logs.
2. Located the Add user activity for Sarah Johnson.
3. Verified the activity status was Success and reviewed the target user information.
4. Located the Add member to group activity.
5. Verified the activity status was Success and confirmed Sarah Johnson and HR-Employees as the targets.
6. Captured screenshots of the activity details and target information.
7. Redacted sensitive identifiers before uploading evidence to GitHub.

## Verification Results
| Control | Observed result |
|---|---|
| User provisioning | Sarah Johnson account successfully created |
| Account type | Member |
| Security group | HR-Employees created |
| Group membership | Sarah Johnson confirmed as a member |
| User creation audit log | Add user activity completed successfully |
| Group membership audit log | Add member to group activity completed successfully |

## Security Concepts Demonstrated
- Identity provisioning
- Group-based access management
- Access control fundamentals
- Administrative verification

## Key Takeaways
Creating a user account establishes an identity within Microsoft Entra ID. Security groups allow administrators to manage access collectively rather than configuring each employee individually. Group membership alone does not grant access to resources unless permissions are separately assigned.

## Scope and Limitations
This lab used Microsoft Entra ID Free. No Microsoft 365 application licenses or HR resource permissions were assigned. The lab verified group membership, not access to an HR application.


## Evidence

The following screenshots document the user provisioning process, security group configuration, and audit log verification.

All screenshots have been reviewed and sensitive identifiers have been redacted before publication.

| Evidence | Description |
|---|---|
| 01 - Group Membership | Confirms Sarah Johnson is a member of HR-Employees |
| 02 - User Account Creation | Verifies the employee account and user properties |
| 03 - Security Group | Shows the security group configuration and assigned membership type |
| 04 - User Creation Audit Log | Confirms successful user creation |
| 04b - User Creation Target | Identifies the target user in the audit event |
| 05 - Group Membership Audit Log | Confirms successful group membership assignment |
| 05b - Group Membership Target | Identifies the user and group associated with the audit event |

[View Lab 01 Evidence](../evidence/)


## Conclusion
Successfully provisioned a fictional employee account, created a departmental security group, assigned membership, and verified the resulting configuration.
