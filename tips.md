---
layout: default
permalink: /all-windows/tips
title: Tips for Recon
---

[Home](index.md) | [Accounts](account.md) | [Authentication](authentication.md)| [Hacking Tools](tools.md) | [Common Ports](ports.md) | [Windows Tool](windowstool.md) | [Powershell](powershell.md) | [Tips](tips.md) 

# Tips 

Windows Active Directory LDAP
You can use https://IP:3269 to check the certificate and CA
openssl s_client -showcerts -connect <IP>:3269 | openssl x509 -noout -text

option 1
cme smb <IP> -u 'xxx' -p '' --shares
cme winrm <IP>
option 2
smbclient -L //<IP>
