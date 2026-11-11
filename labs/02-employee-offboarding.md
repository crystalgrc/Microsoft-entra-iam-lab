# Lab 02: Employee Offboarding and Audit Logging

## Objective
Demonstrate secure employee offboarding, session revocation, account restoration, and audit verification using Microsoft Entra ID.

## Lab Environment
- Microsoft Entra ID Free
- Microsoft Entra Admin Center
- Windows 11
- Microsoft Edge

## Business Scenario
A fictional organization, Contoso Technologies, receives an HR request to terminate Sarah Johnson's access. The IT administrator must disable the account, revoke sign-in sessions, and verify the changes.

A subsequent HR notification indicates the termination was entered in error, requiring the account to be restored.

## Procedure

### 1. Disable the Employee Account
1. Navigated to Entra ID > Users > All users.
2. Selected Sarah Johnson.
3. Opened Edit properties.
4. Changed Account enabled from Yes to No.
5. Saved the change.
6. Verified that the account showed Disabled.

### 2. Revoke Sign-In Sessions
1. Opened Sarah Johnson's account.
2. Selected Revoke sessions.
3. Confirmed the action.

Session revocation invalidates refresh tokens and applicable browser sessions. Previously issued access tokens may remain valid until expiration.

### 3. Verify Audit Evidence
1. Navigated to Entra ID > Monitoring & health > Audit logs.
2. Located the Update user event.
3. Examined the modified properties.
4. Verified the accountEnabled property changed from true to false.

### 4. Restore Employee Access
1. Returned to Sarah Johnson's user account.
2. Changed Account enabled from No to Yes.
3. Saved the change.
4. Verified that the account was enabled.
5. Confirmed that membership in HR-Employees remained intact.

### 5. Verify Restoration Audit Evidence
1. Returned to the Microsoft Entra audit logs.
2. Opened the relevant Update user event.
3. Verified accountEnabled changed from false to true.

## Verification Results

| Control | Observed Result |
|---|---|
| Account disablement | Successful |
| Session revocation | Completed |
| Disablement audit evidence | true to false |
| Account restoration | Successful |
| Restoration audit evidence | false to true |
| HR group membership | Preserved |

## Security Concepts Demonstrated
- Identity lifecycle management
- Employee offboarding
- Account disablement
- Session revocation
- Audit trail verification
- Access restoration
- Security group membership persistence

## Security Considerations
Disabling an account does not necessarily terminate all previously issued access tokens immediately. A complete production offboarding process may also include removing access assignments, reviewing application sessions, securing company devices, and preserving business data according to organizational policies.

## Key Findings
Microsoft Entra ID recorded the account-status changes in directory audit logs. The account was successfully disabled and later restored without removing its HR-Employees group membership.

## Evidence
Screenshots of user status and audit records may be added after removing sensitive identifiers and account information.

## Conclusion
Successfully simulated employee offboarding and restoration while verifying the administrative changes through Microsoft Entra ID audit logs.
