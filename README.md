Ansible Role: Single-Nginx-Site v1.0
===

[![Build Status](https://travis-ci.org/mm0/ansible-role-single-nginx-site.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-single-nginx-site)


An Ansible role that install nginx and sets up a single vhost


Requirements
--

- Sudo access


Role Variables
--

Available variables are listed below:
```yml
- server_domain: hostname.com
```

Dependencies
--

None 

Example Playbook
--

```yml
- hosts: webservers
  vars: 
  - server_domain: hostname.com
  roles:
  - ansible-role-single-nginx-site
```

License
---------------

BSD-2

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github
