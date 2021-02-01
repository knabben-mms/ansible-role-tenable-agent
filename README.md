## ansible-role-tenable-agent
=========

*NOTES*: For now just a dirty fork some work todo   
Ansible role for installing and configuring Nessus Agent

Role Variables
--------------

- `nessus_agent_key`: key used for linking with nessus host (this is a required variable)

- `nessus_agent_group`: host group this agent should be added to when linking with nessus host (this is a required variable)

- `nessus_agent_host`: nessus host to link with (default: `cloud.tenable.com`)

- `nessus_agent_port`: nessus host port (default: `443`)

- `nessus_agent_package`: can be either a repository package, path to a file, or a URL (default: `NessusAgent`)

        nessus_agent_package: nessus-agent
        nessus_agent_package: /tmp/nessus-agent_6.8.1_amd64.deb

Example Playbook
----------------

    - hosts: all
      become: yes
      roles:
         - role: ansible-role-nessus-agent
           nessus_agent_key: xxxxxxxxx
           tags: nessus-agent

TODOs
--------------
- Fixup
- Tests
- CI
- Release Pipeline