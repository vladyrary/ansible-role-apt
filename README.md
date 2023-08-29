Install 5 packages
=========

This role is designed to install five apt packages via Ansible.

Requirements
------------

An ssh connection is required between the master node and the working note
The package name must be valid. For example: vim, traceroute... etc

Role Variables
--------------

Store the name of packages to install in form of array.

Dependencies
------------

None

Example Playbook
----------------

 - name: Playbook to run install 5 packages
   hosts: servers
   become: true
   roles:
     - role: '/root/roles/Install_5_packages'

   - name: Installation 5 packages
     ansible.builtin.package:
       name:
         - nmap
         - traceroute
         - git
         - vim
         - chromium-browser
         - grub-customizer
         - htop
         - apache2
       state: present
       update_cache: yes


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
# ansible-role-apt
