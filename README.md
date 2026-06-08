# arch-ansible

* `sshpass` needed to authenticate to the Arch ISO with no password prompt. 
* `host_key_checking = False` and `UserKnownHostsFile=/dev/null` - Arch ISO regenerates its SSH host key on every boot. If you have installed on the machine before, your `known_hosts` has a stale key and SSH would refuse to connect. This bypasses that. 
* Connect as root on the ISO so no sudo to worry about. 

### ansible.cfg

* no `ansible_password`, instead we pass `--ask-pass` at runtime and type it once. Typing default password once is fine as it allows the file to be free of secrets. 


