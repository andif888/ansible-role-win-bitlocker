# Ansible Role Windows Bitlocker

This role enables Windows Bitlocker for the OS drive using only the TPM as key protector. The recovery password gets store in Active Directory.

## Requirements

The Windows OS has to be joined to an Active Directory Domain. The corresponding computer object has to be in an OU, which has a GPO applied, which configures Bitlocker correctly. 
The GPO has to allow TPM only as key protector. The GPO needs to configure Bitlocker to store the recovery key in Active Directory.

## Example Playbook

```yml
    - hosts: windows-pc
      roles:
         - { role: ansible-role-win-bitlocker }
```

