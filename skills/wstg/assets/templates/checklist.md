# WSTG Execution Checklist — {{PROJECT_NAME}}

**Execution tag:** {{EXECUTION_TAG}}
**Date:** {{DATE}}
**Performed by:** {{PERFORMER}}
**Scope:** {{SCOPE}}
**Standard:** OWASP WSTG v4.2

This checklist is filled in during a single WSTG audit execution. The final state is copied into `test-register.md` as new rows tagged with this execution.

## Legend

| Symbol | Meaning |
|---|---|
| ✅ OK | Test executed, no finding |
| ⚠️ Parcial | Control exists but improvable |
| ❌ Fallo | Confirmed finding (link to issue) |
| ⬜ Pendiente | Requires additional validation |
| N/A | Not applicable |

## INFO — Information Gathering

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-INFO-01 | Search Engine Discovery | | |
| WSTG-v42-INFO-02 | Fingerprint Web Server | | |
| WSTG-v42-INFO-03 | Review Webserver Metafiles | | |
| WSTG-v42-INFO-04 | Enumerate Applications on Webserver | | |
| WSTG-v42-INFO-05 | Review Webpage Content for Leakage | | |
| WSTG-v42-INFO-06 | Identify Application Entry Points | | |
| WSTG-v42-INFO-07 | Map Execution Paths | | |
| WSTG-v42-INFO-08 | Fingerprint Web Application Framework | | |
| WSTG-v42-INFO-09 | Fingerprint Web Application | | |
| WSTG-v42-INFO-10 | Map Application Architecture | | |

## CONF — Configuration and Deployment Management

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-CONF-01 | Network Infrastructure Configuration | | |
| WSTG-v42-CONF-02 | Application Platform Configuration | | |
| WSTG-v42-CONF-03 | File Extensions Handling | | |
| WSTG-v42-CONF-04 | Old Backup and Unreferenced Files | | |
| WSTG-v42-CONF-05 | Admin Interfaces Enumeration | | |
| WSTG-v42-CONF-06 | HTTP Methods | | |
| WSTG-v42-CONF-07 | HTTP Strict Transport Security | | |
| WSTG-v42-CONF-08 | RIA Cross Domain Policy | | |
| WSTG-v42-CONF-09 | File Permission | | |
| WSTG-v42-CONF-10 | Subdomain Takeover | | |
| WSTG-v42-CONF-11 | Cloud Storage | | |

## IDNT — Identity Management

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-IDNT-01 | Role Definitions | | |
| WSTG-v42-IDNT-02 | User Registration Process | | |
| WSTG-v42-IDNT-03 | Account Provisioning Process | | |
| WSTG-v42-IDNT-04 | Account Enumeration | | |
| WSTG-v42-IDNT-05 | Weak Username Policy | | |

## ATHN — Authentication

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-ATHN-01 | Credentials over Encrypted Channel | | |
| WSTG-v42-ATHN-02 | Default Credentials | | |
| WSTG-v42-ATHN-03 | Weak Lock Out Mechanism | | |
| WSTG-v42-ATHN-04 | Bypassing Authentication Schema | | |
| WSTG-v42-ATHN-05 | Vulnerable Remember Password | | |
| WSTG-v42-ATHN-06 | Browser Cache Weaknesses | | |
| WSTG-v42-ATHN-07 | Weak Password Policy | | |
| WSTG-v42-ATHN-08 | Weak Security Question Answer | | |
| WSTG-v42-ATHN-09 | Weak Password Change / Reset | | |
| WSTG-v42-ATHN-10 | Weaker Auth in Alternative Channel | | |

## AUTHZ — Authorization

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-AUTHZ-01 | Directory Traversal / File Include | | |
| WSTG-v42-AUTHZ-02 | Bypassing Authorization Schema | | |
| WSTG-v42-AUTHZ-03 | Privilege Escalation | | |
| WSTG-v42-AUTHZ-04 | Insecure Direct Object References | | |

## SESS — Session Management

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-SESS-01 | Session Management Schema | | |
| WSTG-v42-SESS-02 | Cookies Attributes | | |
| WSTG-v42-SESS-03 | Session Fixation | | |
| WSTG-v42-SESS-04 | Exposed Session Variables | | |
| WSTG-v42-SESS-05 | Cross Site Request Forgery | | |
| WSTG-v42-SESS-06 | Logout Functionality | | |
| WSTG-v42-SESS-07 | Session Timeout | | |
| WSTG-v42-SESS-08 | Session Puzzling | | |
| WSTG-v42-SESS-09 | Session Hijacking | | |

## INPV — Input Validation

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-INPV-01 | Reflected XSS | | |
| WSTG-v42-INPV-02 | Stored XSS | | |
| WSTG-v42-INPV-03 | HTTP Verb Tampering | | |
| WSTG-v42-INPV-04 | HTTP Parameter Pollution | | |
| WSTG-v42-INPV-05 | SQL Injection | | |
| WSTG-v42-INPV-06 | LDAP Injection | | |
| WSTG-v42-INPV-07 | XML Injection | | |
| WSTG-v42-INPV-08 | SSI Injection | | |
| WSTG-v42-INPV-09 | XPath Injection | | |
| WSTG-v42-INPV-10 | IMAP/SMTP Injection | | |
| WSTG-v42-INPV-11 | Code Injection | | |
| WSTG-v42-INPV-12 | Command Injection | | |
| WSTG-v42-INPV-13 | Format String Injection | | |
| WSTG-v42-INPV-14 | Incubated Vulnerability | | |
| WSTG-v42-INPV-15 | HTTP Splitting / Smuggling | | |
| WSTG-v42-INPV-16 | HTTP Incoming Requests | | |
| WSTG-v42-INPV-17 | Host Header Injection | | |
| WSTG-v42-INPV-18 | Server-Side Template Injection | | |
| WSTG-v42-INPV-19 | Server-Side Request Forgery | | |
| WSTG-v42-INPV-20 | Mass Assignment | | |

## ERRH — Error Handling

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-ERRH-01 | Improper Error Handling | | |
| WSTG-v42-ERRH-02 | Stack Traces | | |

## CRYP — Cryptography

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-CRYP-01 | Weak Transport Layer Security | | |
| WSTG-v42-CRYP-02 | Padding Oracle | | |
| WSTG-v42-CRYP-03 | Sensitive Info over Unencrypted Channels | | |
| WSTG-v42-CRYP-04 | Weak Encryption | | |

## BUSL — Business Logic

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-BUSL-01 | Business Logic Data Validation | | |
| WSTG-v42-BUSL-02 | Ability to Forge Requests | | |
| WSTG-v42-BUSL-03 | Integrity Checks | | |
| WSTG-v42-BUSL-04 | Process Timing | | |
| WSTG-v42-BUSL-05 | Number of Times a Function Can Be Used | | |
| WSTG-v42-BUSL-06 | Circumvention of Work Flows | | |
| WSTG-v42-BUSL-07 | Defenses Against Application Misuse | | |
| WSTG-v42-BUSL-08 | Upload of Unexpected File Types | | |
| WSTG-v42-BUSL-09 | Upload of Malicious Files | | |

## CLNT — Client-Side

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-CLNT-01 | DOM-Based XSS | | |
| WSTG-v42-CLNT-02 | JavaScript Execution | | |
| WSTG-v42-CLNT-03 | HTML Injection | | |
| WSTG-v42-CLNT-04 | Client-side URL Redirect | | |
| WSTG-v42-CLNT-05 | CSS Injection | | |
| WSTG-v42-CLNT-06 | Client-side Resource Manipulation | | |
| WSTG-v42-CLNT-07 | CORS | | |
| WSTG-v42-CLNT-08 | Cross Site Flashing | | |
| WSTG-v42-CLNT-09 | Clickjacking | | |
| WSTG-v42-CLNT-10 | WebSockets | | |
| WSTG-v42-CLNT-11 | Web Messaging | | |
| WSTG-v42-CLNT-12 | Browser Storage | | |
| WSTG-v42-CLNT-13 | Cross Site Script Inclusion | | |
| WSTG-v42-CLNT-14 | Reverse Tabnabbing | | |

## APIT — API Testing

| ID | Test | Status | Evidence / Notes |
|---|---|---|---|
| WSTG-v42-APIT-01 | GraphQL | | |

## Summary

| Status | Count |
|---|---|
| ✅ OK | |
| ⚠️ Parcial | |
| ❌ Fallo | |
| ⬜ Pendiente | |
| N/A | |
| **Total** | |

## Notes

_(Free-form notes about scope decisions, tooling used, environment, and any deviations from the standard protocol.)_
