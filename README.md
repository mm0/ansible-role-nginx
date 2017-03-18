Ansible Role: Single-Nginx-Site v1.0
===

[![Build Status](https://travis-ci.org/mm0/ansible-role-single-nginx-site.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-single-nginx-site)


An Ansible role that install nginx and sets up a single vhost

The role automaticall sets up HTTP -> HTTPS redirects and creates HTTPS Listeners for naked domain and www.subdomain

Keys are required for SSL configuration by specifying the paths

Requirements
--

- Sudo access


Role Variables
--

Available variables are listed below:
```yml
- server_domain: hostname.com
naked_domain_keys:
  private: /etc/letsencrypt/live/2m.io/privkey.pem;
  fullchain: /etc/letsencrypt/live/2m.io/fullchain.pem;
www_domain_keys:
  private: /etc/letsencrypt/live/dev.2m.io/privkey.pem;
  fullchain: /etc/letsencrypt/live/dev.2m.io/fullchain.pem;
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
