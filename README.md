Common
======================

Ansible role
------------

These variables could be configured:

- **do_upgrade**: if _yes_ performs an apt upgrade, if _dist_ performs a dist-upgrade.
- **allow_tcp_ports**: list of tcp port numbers to allow in the firewall
- **allow_tcp_ports_from**: list of tcp port numbers to restrict connections in the firewall 
   only from a list of sources. Each item must have the _port_ field with the port number and 
   the _from_ field with the list of allowed ips.
- **limit_ssh_from**: restrict ssh from specified ips
- **authorized_ssh_keys**: list of ssh keys
- **icinga_server**: Address of icinga server. If defined, this role installs nrpe packages
  and configure nrpe to allow the specified icinga server to run checks.
- **nrpe_systemd_services**: list of service names that could be checked by nrpe. For each one
  it is created a check named _check_name_service_, where name is the name in the list.
- **nrpe_custom_commands**: A list of objects to define custom nrpe checks. Each item must contain the _name_ field and
  the _check_ field with the nagios check command to run.
  
