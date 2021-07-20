# Ansible Role: Winbind
An Ansible Role that joins Linux machines (Debian and CentOS) to Windows Active Directory with Winbind. This was originally developed when I was having trouble authenticating with SSSD.

## Example Playbook
```yaml
---
- hosts: all
  become: yes
  gather_facts: yes
  tasks:
    - name: Include the role ansible-role-windbind
      ansible.builtin.include_role:
        name: ckstevenson.winbind
```
## License 
MIT / BSD
