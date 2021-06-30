# Ansible Role: Winbind
An Ansible Role that joins Linux machines (Debian and CentOS) to Windows Active Directory with Winbind. This was originally developed when I was having trouble authenticating with SSSD.

## Example Playbook
```yaml
---
- hosts: all
  become: yes
  gather_facts: yes
  vars:
    workgroup:
    domain:
    ad_path:
    ad_username:
    ad_password:
    ntp:
      -
      -
    firewalld: false
  tasks:
    - name: Include the role ansible-role-windbind
      ansible.builtin.include_role:
        name: ckstevenson.winbind
        tasks_from: "{{ ansible_distribution|lower }}"
```
## License 
MIT / BSD
