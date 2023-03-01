User-Domain
=========

This role deploys the domain user account on my newly created virtual machine. It also deploys ssh-keys for connections. 

Requirements
------------

This playbook assumes ansible can already connect to the machine. The machine must also be joined to the domain.

Role Variables
--------------
Required variables are listed here, along with default example values. See defaults/main.yml.

    domain_user: username

This is the user to be deployed on the system. 

Dependencies
------------

domain-join

Example Playbook
----------------

    # Deploys the domain user account on the host.
    - name: Add the domain user account.
      hosts: deploy
      become: true
      roles:
        - role: user-domain

License
-------

BSD

Author Information
------------------

Derek Smiley - Network Analyst, Homelabber, aspiring System Administrator/Ansible Automation Engineer

Connect with me on LinkedIn - https://www.linkedin.com/in/derek-smiley/

Much of this was created using snippets from other public repositories on github. I claim ownership of none of this code.