
# Lab 02: Employee Offboarding — Evidence

## Overview
This folder contains screenshots documenting the employee offboarding process in Microsoft Entra ID.

## Evidence Checklist

| Evidence | Description |
|---|---|
| 01 - Account Enabled Before | Verifies Sarah Johnson's account was enabled before offboarding |
| 02 - Account Disabled | Confirms the employee account was disabled |
| 03 - Sessions Revoked | Documents successful sign-in session revocation |
| 04 - Group Membership Before | Shows original membership in HR-Employees |
| 05 - Group Membership After | Confirms removal from HR-Employees |
| 06 - Audit Session Revocation | Shows the StsRefreshTokensValidFrom property change |
| 07 - Audit Account Disabled | Shows the AccountEnabled property changed from True to False |
| 08 - Audit Group Removal | Verifies successful group membership removal |
| 08b - Audit Group Removal Target | Identifies the affected user and security group |

## Security and Privacy
Sensitive identifiers, tenant information, and personal account details have been redacted before publication.

## Related Documentation
[Lab 02: Employee Offboarding](../../labs/02-employee-offboarding.md)
