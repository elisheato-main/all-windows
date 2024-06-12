---
layout: default
title: Powershell Commands
---

[Home](index.md) | [Accounts](account.md) | [Authentication](authentication.md)| [Hacking Tools](tools.md) | [Common Ports](ports.md) | [Windows Tool](windowstool.md) | [Powershell](powershell.md)

## Powershell Commands

| Command              | Description                                                                                       | Usage                                                      | Examples                                                                                                         |
|----------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `Get-Process`        | Retrieves information about the processes running on the system.                                  | `Get-Process`                                              | Retrieves a list of all processes currently running on the system.                                                |
| `Get-Service`        | Retrieves information about the services installed on the system.                                  | `Get-Service`                                              | Retrieves a list of all services currently installed on the system.                                                |
| `Get-EventLog`       | Retrieves event log entries from one or more event logs on the local or remote computers.          | `Get-EventLog [-LogName] [-ComputerName] [-InstanceId]`    | Retrieves event log entries from the Application log on the local computer.                                         |
| `Get-WmiObject`      | Retrieves instances of Windows Management Instrumentation (WMI) classes or information about them. | `Get-WmiObject [-Class] [-Namespace] [-ComputerName]`       | Retrieves information about the operating system version using the Win32_OperatingSystem class.                   |
| `Get-ADUser`         | Retrieves one or more Active Directory user objects.                                              | `Get-ADUser [-Identity] [-Filter]`                         | Retrieves information about the user with the username "JohnDoe".                                                  |
| `Get-ADUser`         | Retrieves one or more Active Directory user objects.                                              | `Get-ADUser [-Identity] [-Properties]`                     | Retrieves information about the user with the username "JohnDoe" and specific properties like email, phone number, etc. |
| `Get-ADUser`         | Retrieves one or more Active Directory user objects.                                              | `Get-ADUser [-Filter] | -SearchBase | -SearchScope | -ResultSetSize`  | Retrieves information about users based on specific filters, search bases, search scopes, and result set sizes.   |
| `New-Item`           | Creates a new item, such as a file or directory.                                                  | `New-Item [-Path] [-ItemType] [-Name]`                     | Creates a new directory named "NewFolder" in the current directory.                                                |
| `Remove-Item`        | Deletes an item, such as a file or directory.                                                     | `Remove-Item [-Path] [-Recurse]`                           | Deletes the file "OldFile.txt" from the current directory.                                                         |
| `Copy-Item`          | Copies an item, such as a file or directory.                                                      | `Copy-Item [-Path] [-Destination]`                         | Copies the file "Template.docx" to the "Backup" directory.                                                          |
| `Move-Item`          | Moves an item, such as a file or directory.                                                       | `Move-Item [-Path] [-Destination]`                         | Moves the directory "Folder1" to the "Archive" directory.                                                          |
| `Set-ExecutionPolicy`| Sets the PowerShell script execution policy for the computer.                                      | `Set-ExecutionPolicy [-ExecutionPolicy]`                   | Sets the execution policy to "RemoteSigned".                                                                        |
| `Get-Help`           | Displays help information for PowerShell cmdlets, functions, scripts, and modules.                 | `Get-Help [-Name] [-Full]`                                | Displays detailed help information for the `Get-Service` cmdlet.                                                    |
| `Start-Process`      | Starts one or more processes on the local computer.                                                | `Start-Process [-FilePath] [-ArgumentList]`                | Starts the Notepad application.                                                                                    |
| `Invoke-Command`     | Runs commands on local and remote computers.                                                       | `Invoke-Command [-ScriptBlock] [-ComputerName]`            | Runs the `Get-Service` cmdlet on a remote computer named "Server01".                                                |
| `Get-ChildItem`      | Retrieves the child items (files and directories) in a specified location.                         | `Get-ChildItem [-Path] [-Recurse]`                        | Retrieves a list of all files and directories in the current directory and its subdirectories.                    |
| `Get-Content`        | Retrieves the content of a file.                                                                  | `Get-Content [-Path]`                                      | Displays the contents of the file "Example.txt".                                                                   |
| `Set-Content`        | Writes or replaces the content of a file.                                                         | `Set-Content [-Path] [-Value]`                             | Writes the text "Hello, world!" to the file "Greeting.txt".                                                        |
| `Test-Connection`    | Tests network connectivity to a specified computer by sending ICMP echo request packets ("ping").  | `Test-Connection [-ComputerName] [-Count]`                 | Tests network connectivity to the computer "Server01" by sending 4 ICMP echo requests.                              |
| `Test-Path`          | Determines whether all elements of a path exist on the local computer.                              | `Test-Path [-Path]`                                        | Checks if the file "Example.txt" exists in the current directory.                                                   |
| `Get-LocalUser`      | Retrieves information about local user accounts on the computer.                                    | `Get-LocalUser`                                            | Retrieves a list of all local user accounts on the computer.                                                        |
| `Get-LocalGroupMember` | Retrieves the members of a local group on the computer.                                             | `Get-LocalGroupMember [-Group]`                           | Retrieves a list of members of the "Administrators" group on the computer.                                          |