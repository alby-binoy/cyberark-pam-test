# CyberArk PAM Components

CyberArk PAM consists of several components that work together to secure and manage privileged accounts.

## 1. Digital Vault

The Digital Vault is the secure storage component of CyberArk.

It is responsible for securely storing sensitive information such as:

- Privileged account credentials
- Passwords
- Encryption keys
- Other sensitive authentication information

The Vault is a critical security component because it protects the credentials managed by the PAM solution.

## 2. PVWA - Password Vault Web Access

PVWA provides a web-based interface for users and administrators to interact with CyberArk.

Common activities include:

- Searching for accounts
- Requesting access
- Viewing account information
- Managing Safes
- Initiating privileged sessions
- Performing administrative tasks

Users typically interact with CyberArk through PVWA rather than directly accessing the Vault.

## 3. CPM - Central Policy Manager

CPM is responsible for automated password management.

It can perform tasks such as:

- Changing passwords
- Verifying passwords
- Reconciling passwords
- Enforcing password management policies

For example, when a privileged account is configured for automatic password rotation, CPM can change the password according to the configured policy.

## 4. PSM - Privileged Session Manager

PSM provides controlled access to privileged sessions.

It can be used to connect users to target systems without exposing the privileged password directly to the user.

PSM can also provide session monitoring and recording capabilities, depending on the organization's configuration and requirements.

Examples of sessions that may be managed include:

- RDP
- SSH
- Other supported protocols and applications

## 5. How the Components Work Together

A simplified flow can be represented as:

User
  |
  v
PVWA
  |
  v
Digital Vault
  |
  +----> CPM
  |       |
  |       +---- Password Management
  |
  +----> PSM
          |
          +---- Privileged Session
                  |
                  v
             Target Server

The exact architecture can vary depending on the CyberArk deployment.

## Quick Comparison

Component | Main Purpose 
|---|---|
| Digital Vault | Secure storage of privileged credentials and sensitive information |
| PVWA | Web interface for CyberArk users and administrators |
| CPM | Automated password management |
| PSM | Controlled and monitored privileged sessions |

## Key Takeaway

A simple way to remember the major components is:

- **Vault → Stores**
- **PVWA → Provides access/interface**
- **CPM → Manages passwords**
- **PSM → Manages sessions**

> **Note:** This document is for learning purposes. No confidential company information, credentials, internal infrastructure details, or proprietary configuration is included.
