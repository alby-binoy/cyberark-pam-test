# CyberArk Safes and Permissions

## What is a Safe?

A Safe is a logical container in CyberArk used to securely store and manage accounts and credentials.

A Safe can contain multiple accounts.

For example:

```text
Safe: Linux-Production

    ├── root@server01
    ├── root@server02
    ├── appadmin@server01
    └── oracle@server03
