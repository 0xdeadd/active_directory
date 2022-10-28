# Installing the Domain Controller

1. Use `sconfig` to:
    - Change the hostname
    - Change the IP address to static
    - Change the DNS server to itself
2. Install the Active Directory Windows Feature

```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```
# Joining the Workstation to the domain

```shell
Add-Computer -Domainname xyz.com -Credential xyz\Administrator -Force -Restart
```