---
layout: default
title: Windows Accounts
---

- [Home](index.md) | [Accounts](account.md) | [Hacking Tools](tools.md) | [Common Ports](ports.md)

## Windows Accounts

| **Account Type**              | **Account Name**        | **Example Account Name**         | **Usage**                                                                                       |
|-------------------------------|-------------------------|----------------------------------|-------------------------------------------------------------------------------------------------|
| Built-in Administrator        | Administrator           | Administrator                    | The default local administrator account with full system access. Used for managing the server.  |
| Built-in Guest                | Guest                   | Guest                            | Limited access account. Disabled by default. Used for temporary access without permanent account creation. |
| Default Service Accounts      | LocalSystem             | LocalSystem                      | Highly privileged account used by the operating system. Runs system services and has extensive privileges. |
|                               | LocalService            | LocalService                     | Less privileged account than LocalSystem. Used to run services with limited access to resources. |
|                               | NetworkService          | NetworkService                   | Similar to LocalService but with network credentials. Used to run services that require network access. |
| Domain Accounts               | Domain Admins           | AD/Domain Admins                 | Group whose members have administrative privileges across the domain. Used for managing the domain. |
|                               | Specific Domain Users   | AD/jdoe, AD/asmith               | Actual user accounts within an Active Directory domain. Used for general user access and activities. |
|                               | Domain Guests           | AD/Domain Guests                 | Guest accounts within a domain. Disabled by default. Used for temporary access within a domain. |
| Group Managed Service Accounts| gMSA                    | AD/sqlgmsa                       | Managed service account for services running across multiple servers, with automatic password management. |
| Special Accounts              | SYSTEM                  | SYSTEM                           | Used by the operating system. Has extensive privileges similar to LocalSystem.                  |
|                               | DefaultAccount          | DefaultAccount                   | Built-in account for system use, present in Windows 10 and later.                               |
|                               | WDAGUtilityAccount      | WDAGUtilityAccount               | Used by Windows Defender Application Guard.                                                     |
| Administrative Accounts       | Local Administrator     | AdminUser1                       | User-created administrator accounts. Used for administrative tasks on the local machine.        |
|                               | Domain Administrator    | AD/domadmin1                     | User-created accounts with administrative privileges across the domain. Used for managing domain resources. |
| Standard User Accounts        | Local User              | user1                            | User-created accounts with standard privileges. Used for daily non-administrative tasks.        |
|                               | Domain User             | AD/domuser1                      | User-created accounts within a domain with standard privileges. Used for daily non-administrative tasks. |
| SQL Server Service Account    | SQLServer               | SQLServer                        | The account used by the SQL Server service to run the SQL Server database engine.               |
| SQL Server System Administrator (sa) | sa               | sa                               | The default system administrator account in SQL Server with full privileges.                   |
| NT AUTHORITY\SYSTEM           | NT AUTHORITY\SYSTEM     | NT AUTHORITY\SYSTEM              | Represents the LocalSystem account in SQL Server, having high privileges similar to LocalSystem in Windows. |
| NT SERVICE\MSSQLSERVER        | NT SERVICE\MSSQLSERVER  | NT SERVICE\MSSQLSERVER           | Service account for the SQL Server Database Engine service.                                      |
| NT SERVICE\SQLSERVERAGENT     | NT SERVICE\SQLSERVERAGENT | NT SERVICE\SQLSERVERAGENT      | Service account for the SQL Server Agent service, if installed.                                   |
| IIS Application Pool Accounts | IIS AppPool\DefaultAppPool | IIS AppPool\MyAppPool          | Accounts used by IIS application pools to run web applications.                                 |
| Application-Specific Accounts | APS (Application Pool Service) | APSUser1                   | Custom service accounts created for specific applications.                                      |

## Windows Generic Accounts

| **Account Type**         | **Example Account Name** | **Usage**                                                                                   | **Permissions**                                                                   |
|--------------------------|---------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Service Account          | SQLServer                 | Used by services to run processes or applications, often associated with specific services. | Permissions are determined by the service they are associated with.             |
| System Account           | NT AUTHORITY\SYSTEM       | A built-in account used by the operating system itself and services running as LocalSystem. | Has extensive privileges, often used for system-level tasks and services.        |
| Administrator            | Administrator            | The default local administrator account with full system access.                           | Has full control over the system, including installation, configuration, etc.    |
| Guest                    | Guest                    | Limited access account, disabled by default, used for temporary access.                     | Has minimal privileges and is typically used for guest users.                    |
| Built-in Service Accounts| LocalService             | Used by system services with limited access to resources.                                   | Has limited privileges, typically used to run services with restricted access.   |
|                          | NetworkService           | Similar to LocalService but with network credentials.                                       | Has network access privileges, used to run network services.                     |
|                          | LocalSystem              | A built-in account with extensive privileges, used to run system services.                  | Has extensive privileges, often used for system-level tasks and services.        |
|                          | DefaultAccount           | A built-in account for system use, present in Windows 10 and later.                         | Used for system-level tasks and services.                                        |
|                          | WDAGUtilityAccount       | Used by Windows Defender Application Guard.                                                 | Used for specific security-related tasks.                                        |
| Domain User              | AD\jdoe                  | User accounts within a domain with standard privileges.                                     | Permissions depend on the user's group memberships and domain policies.           |
