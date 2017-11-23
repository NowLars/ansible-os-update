# ansible-os-update
Ansible playbook to update all Unix and Linux hosts you manage.

An playbook to update systems on differend kind of Unix and Linux OS distributions.
Using the native distribution packaging system. Checks for required reboots and execute a reboot.


## Current supported operating systems distributions
- GNU/Linux Debian
- GNU/Linux Centos
- GNU/Linux RedHat
- Unix FreeBSD
- Unix Smartos

## Usage

### Do Update
```
ansible-playbook main.yml
```
### Custom configuration

see group_vars/all

|Var|Values|Usage|
|---|:----:|-----|
|reboot_timeout|integer|timeout in seconds to wait for host to respond after reboot|
|wait_for_host_after_reboot|boolean|enable wait for host to respond after reboot|
|update_logs|boolean|write update output to logfiles|
|smartos_pkgin_global_zone|boolean|run pkgin update in Solaris derived systems global zone|

