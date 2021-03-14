# ansible-os-update
Ansible playbook to update all Unix and Linux hosts you manage.

An playbook to update systems on differend kind of Unix and Linux OS distributions.
Using the native distribution packaging system. Checks for required reboots and execute a reboot.


## Current supported operating system distributions

|System|OS Family| Distributions |Tested Distributions| Tested Arch|
|:----:|:-------:|---------------|--------------------|------------|
|GNU/Linux|Debian| Debian,Ubuntu,... | Debian| amd64,armv6l |
|GNU/Linux|RedHat| RedHat,Centos,OracleLinux | Centos | amd64 |

more distributions can follow

## Usage

- clone this repo
- install ansible
- create ansible inventory
- run ansble-playbook

### Run playbook
```
ansible-playbook main.yml
```
### Custom configuration

see group_vars/all

|Var|Values|Usage|
|---|:----:|-----|
|reboot_host|boolean|reboot host autmatically when needed|
|reboot_timeout|integer|timeout in seconds to wait for host to respond after reboot|
|wait_for_host_after_reboot|boolean|enable wait for host to respond after reboot|
