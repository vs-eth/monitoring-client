# Icinga

Configure icinga for SOSETH client use. This is what gets installed on every node,
just like syslog forwarding. All checks are stored as a local fact which gets read
by the master node playbook.
Checks configured automatically:
* ceph
* mem
* iostat
* raid
* load
* ssh
* apt
* icinga
* procs
* users

Checks configured manually:
* ipmi: Set ipmi_hosts to a list of dicts, where each entry has the following attributes:
** name: The (icinga'd) name of the host the IPMI belongs to (replace . by \_)
** ip: The IP the IPMI is available on
