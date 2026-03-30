# Identity Provider Lab – Keycloak & OAuth 2.0

A home lab where I deployed Keycloak as an open source Identity Provider to understand how modern IAM platforms work under the hood – OAuth 2.0, OpenID Connect, SSO, and MFA in practice.

---

## Overview

Platforms like Azure AD, Okta, and AWS IAM are all built on the same protocols as Keycloak. Setting this up myself gave me a practical understanding of how authentication and authorization actually work – not just what buttons do in a GUI.

---

## Tools & Technologies

- Keycloak 23 (deployed via Docker)
- Docker Compose
- OAuth 2.0 / OpenID Connect (OIDC)
- A test application for verifying authentication flows

---

## What I Did

### Setup
- Deployed Keycloak using Docker Compose
- Configured an admin account and accessed the Keycloak Admin Console

### Realm & Users
- Created a new realm (`lab-realm`) isolated from master
- Added test users and assigned roles (admin, user, read-only)
- Configured password policies and session timeout rules

### OAuth 2.0 & OpenID Connect
- Registered a client application in Keycloak
- Implemented the Authorization Code Flow with OIDC
- Verified that JWT tokens contained the correct claims and roles

### Single Sign-On (SSO)
- Configured SSO so one login session applies across multiple applications in the same realm
- Tested and verified the SSO flow end-to-end

### Multi-Factor Authentication (MFA)
- Enabled TOTP (time-based one-time password) as a second factor
- Set MFA as mandatory for the admin role
- Tested the full authentication flow with and without MFA active

---

## Key Takeaways

- How OAuth 2.0 and OIDC work in practice, not just in theory
- Why SSO reduces security risk compared to separate passwords per system
- How MFA adds a second layer without breaking the user experience
- Directly applicable to enterprise platforms: Azure AD / Entra ID, Okta, AWS IAM

---

## Related Concepts

`Keycloak` `IAM` `OAuth 2.0` `OpenID Connect` `SSO` `MFA` `RBAC` `JWT` `Azure AD` `Identity Management`
