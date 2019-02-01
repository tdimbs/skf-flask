## Description:

In scenarios where the application does not properly terminates user active sessions after user role modification, implementation of new administrative functionalities or other enrollments, such as Multi-Factor-Authentication (MFA), transactions restrictions and etc., an malicious user may misuse the entitlements granted previously and have unauthorized access to functionalities which are now blocked.


## Solution:

After rolling out high-value action (password changes, profile updates, MFA enrollment) or administrative functionalities updates, make sure to forcebly terminate every active user session and enforce re-authentication, making sure all authorizations and entitlements are correctly granted to new sessions. 
