
# Lab 02: Employee Offboarding and Audit Logging

## Objective

Demonstrate secure employee offboarding, account disablement, session revocation, security group membership removal, and audit verification using Microsoft Entra ID.

## Lab Environment

- Microsoft Entra ID Free
- Microsoft Entra Admin Center
- Windows 11
- Microsoft Edge

## Business Scenario

A fictional organization, Contoso Technologies, receives an HR request to terminate Sarah Johnson's access following her departure from the organization.

The IT administrator must disable her account, revoke sign-in sessions, remove departmental security group membership, and verify the administrative changes through audit logs.

This lab builds on Lab 01: User Provisioning and Group Management.

## Procedure

### 1. Verify Existing Employee Access

1. Navigated to Microsoft Entra ID > Users > All users.
2. Selected Sarah Johnson.
3. Verified that the employee account was enabled.
4. Confirmed membership in the HR-Employees security group.
5. Captured baseline evidence before offboarding.

### 2. Disable the Employee Account

1. Opened Sarah Johnson's account properties.
2. Changed Account enabled from Yes to No.
3. Saved the change.
4. Verified that the account showed Disabled.
5. Captured evidence of the disabled account.

### 3. Revoke Sign-In Sessions

1. Opened Sarah Johnson's account overview.
2. Selected Revoke sessions.
3. Confirmed the action.
4. Received confirmation that sessions were successfully revoked.

Session revocation invalidates refresh tokens and applicable browser sessions. Previously issued access tokens may remain valid until expiration.

### 4. Remove Security Group Membership

1. Navigated to Sarah Johnson's group memberships.
2. Verified membership in HR-Employees.
3. Selected the HR-Employees security group.
4. Removed the employee's membership.
5. Confirmed successful removal.
6. Captured evidence before and after the change.

### 5. Verify Audit Evidence

Navigated to Microsoft Entra ID > Monitoring & health > Audit logs.

#### Account Disablement

- Located the account disablement activity.
- Reviewed the modified properties.
- Verified AccountEnabled changed from True to False.

#### Session Revocation

- Located the relevant Update user activity.
- Reviewed the Modified Properties tab.
- Identified the StsRefreshTokensValidFrom property.
- Verified that the refresh token validity timestamp was updated.

Observed values:

| Property | Old Value | New Value |
|---|---|---|
| StsRefreshTokensValidFrom | 2026-11-15T23:55:11Z | 2026-11-15T23:55:30Z |

The updated timestamp provides audit evidence that the user's refresh token validity settings changed during session revocation.

#### Security Group Removal

- Located the Remove member from group activity.
- Verified the activity completed successfully.
- Reviewed the target information.
- Confirmed Sarah Johnson and HR-Employees were associated with the removal event.

## Verification Results

| Control | Observed Result |
|---|---|
| Initial account status | Enabled |
| Account disablement | Successful |
| Final account status | Disabled |
| Session revocation | Successful |
| Session revocation audit evidence | StsRefreshTokensValidFrom timestamp updated |
| Disablement audit evidence | AccountEnabled changed from True to False |
| HR-Employees membership removal | Successful |
| Group removal audit evidence | Remove member from group activity verified |
| Identity record | Retained for administrative and audit purposes |

## Security Concepts Demonstrated

- Identity lifecycle management
- Employee offboarding
- Account disablement
- Session and refresh token revocation
- Group-based access management
- Least privilege
- Audit trail verification
- Administrative accountability

## Security Considerations

Disabling an account prevents new sign-ins but does not necessarily terminate all previously issued access tokens immediately.

Session revocation helps reduce the risk of continued access through existing sessions.

Removing security group membership removes group-based access assignments associated with that membership.

A complete production offboarding process may also include reviewing direct application assignments, removing privileged roles, securing company devices, transferring business data, and following organizational retention policies.

## Key Findings

Microsoft Entra ID recorded the administrative changes in directory audit logs.

Session revocation was identified through the StsRefreshTokensValidFrom modified property rather than relying solely on the activity name.

The employee account was disabled, sign-in sessions were revoked, and HR-Employees membership was removed. The identity record was retained for administrative and audit purposes.

## Scope and Limitations

This lab used Microsoft Entra ID Free and a fictional employee account.

No Microsoft 365 application licenses or HR resource permissions were assigned. The lab verified directory configuration changes and audit events, not access to a production application.

No live application session was tested.

The employee account remains disabled. Account restoration was not performed during this lab.

## Evidence

The following screenshots document the employee offboarding process and audit verification.

| Evidence | Description |
|---|---|
| 01 - Account Enabled Before | Initial employee account status |
| 02 - Account Disabled | Disabled employee account |
| 03 - Sessions Revoked | Successful session revocation |
| 04 - Group Membership Before | Original HR-Employees membership |
| 05 - Group Membership After | Successful membership removal |
| 06 - Audit Session Revocation | Refresh token validity timestamp change |
| 07 - Audit Account Disabled | AccountEnabled changed from True to False |
| 08 - Audit Group Removal | Successful group removal activity |
| 08b - Audit Group Removal Target | Affected user and security group |

Sensitive identifiers and account information have been redacted before publication.

[View Lab 02 Evidence](../evidence/lab-02-employee-offboarding/)

## Conclusion

Successfully simulated employee offboarding using Microsoft Entra ID by disabling the employee account, revoking sign-in sessions, removing departmental security group membership, and verifying the administrative changes through audit logs.

This lab demonstrates practical identity lifecycle management and security auditing skills, building on the user provisioning and group management exercises completed in Lab 01.
