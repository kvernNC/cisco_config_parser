cisco_config_parser
=========

A role using ansible-network.network-engine's command_parser to generate host_vars of ios device from the running-config.

A more complete and lighter alternative to ios_facts.

Requirements
------------
privilege 15 on the device to be able to run showr

vars retrieved
--------------

- hostname
- major version
- aaa
- vlan
- vrf
- interfaces
- line
- ... (more to come)
(check my example in tests/host_vars/CSR1000v1)

Dependencies
------------

Ansible-network.network-engine

How to test it
----------------

- git clone https://github.com/kvernNC/cisco_config_parser.git
- cd cisco_config_parser/tests/
- ansible-galaxy install -r roles/requirements.yml
- edit inventory and group_vars for adding your device
- ansible-playbook test.yml
- check the result in host_vars

License
-------

BSD

Author Information
------------------

Kvern, contact me via github.
