My_role
=========

A simple role to test my own ansible module written in python

Requirements
------------

No prerequisites

Role Variables
--------------

There are 4 variables with default values:
my_module_name: "hello"
my_module_new: True
my_module_path: "/tmp/my_module.txt" 
my_module_content: "upopabylasobaka"

Dependencies
------------


Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: my_role }

License
-------

MIT

Author Information
------------------

Wrotten during devops study