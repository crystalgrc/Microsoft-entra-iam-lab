# Lab 03: Role-Based Access Control (RBAC) and Least Privilege

## Objective
Demonstrate role-based access control, least-privilege administration, and separation of duties using Microsoft Entra ID.

## Lab Environment
- Microsoft Entra ID Free
- Microsoft Entra Admin Center
- Windows 11
- Microsoft Edge InPrivate browsing

## Business Scenario
Contoso Technologies has hired Michael Davis as an IT Helpdesk Technician. He needs permission to perform authorized password resets without receiving unrestricted administrative access.

The IT administrator must assign an appropriate role and verify its permissions.

## Procedure

### 1. Create the Helpdesk Account
1. Navigated to Microsoft Entra ID > Users > All users.
2. Created a fictional employee account for Michael Davis.
3. Verified that the account was successfully provisioned.

### 2. Assign the Administrative Role
1. Opened Michael Davis's account.
2. Assigned the Helpdesk Administrator role.
3. Verified that Michael had the intended administrative role.
4. Confirmed that Global Administrator was not assigned.

### 3. Test Delegated Administration
1. Opened Microsoft Edge in an InPrivate window.
2. Signed into the Microsoft Entra Admin Center as Michael Davis.
3. Navigated to Sarah Johnson's user account.
4. Verified that Michael could perform an authorized password reset.
5. Successfully reset Sarah's password.

### 4. Test Privilege Restrictions
1. Attempted to assign the Global Administrator role while signed in as Michael.
2. Confirmed that the action was not permitted.
3. Attempted to access directory audit logs.
4. Confirmed that Michael did not have the required permissions.

### 5. Verify Administrative Activity
1. Signed into Microsoft Entra ID using the lab Global Administrator account.
2. Navigated to the directory audit logs.
3. Located the password-reset event.
4. Verified that Michael Davis was identified as the initiating administrator.

### 6. Conduct a Manual Access Review
Reviewed the administrative role assignments for the lab accounts:

| Account | Administrative Role |
|---|---|
| Lab administrator | Global Administrator |
| Michael Davis | Helpdesk Administrator |
| Sarah Johnson | None |

## Verification Results

| Security Control | Observed Result |
|---|---|
| Helpdesk Administrator assignment | Successful |
| Password reset for Sarah Johnson | Successful |
| Global Administrator role assignment attempt | Not permitted |
| Audit log access as Michael | Not permitted |
| Password-reset audit evidence | Verified |
| Manual administrative access review | Completed |

## Security Concepts Demonstrated
- Role-Based Access Control (RBAC)
- Principle of least privilege
- Delegated administration
- Separation of duties
- Privileged access management fundamentals
- Administrative audit logging
- Access review procedures

## Security Analysis
The Helpdesk Administrator role allowed Michael Davis to perform a permitted support function without granting unrestricted administrative privileges.

Testing confirmed that Michael could reset the selected user's password but could not assign the Global Administrator role or access directory audit logs.

These observations demonstrate how delegated administration can reduce unnecessary privileged access.

The results apply to the accounts, roles, and configuration tested in this lab. Microsoft Entra permissions can vary based on role assignments, target accounts, and directory configuration.

## Key Findings
1. Administrative roles can restrict access to specific operational responsibilities.
2. A Helpdesk Administrator does not require Global Administrator privileges to perform supported password resets.
3. Unauthorized administrative operations were restricted in the tested configuration.
4. Audit logs provided evidence of the administrator responsible for the password-reset action.
5. Manual access reviews help identify excessive or unnecessary privileges.

## Scope and Limitations
This lab used Microsoft Entra ID Free and manually tested selected role permissions. It did not implement Privileged Identity Management, automated access reviews, or production access governance workflows.

## Evidence
Screenshots of role assignments, restricted actions, and audit events may be added after redacting tenant identifiers, usernames, and sensitive information.

## Conclusion
Successfully implemented and tested delegated administration using Microsoft Entra ID. Verified that the Helpdesk Administrator role supported authorized password-reset operations while restricting higher-privilege activities.

The exercise demonstrated practical application of RBAC, least privilege, separation of duties, and administrative audit verification.
