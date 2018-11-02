nginx_site_removal
=========

Ansible role that removes one or more new virtual hosts on an NginX webserver.

Requirements
------------

You'll need to have NginX already setup and working on the server you are running this role on.

Role Variables
--------------

Sites to setup and host on the webserver
```
	nginx_site_removal_sites_to_remove:
	  - {
		  url: 'mysite.com',
		  name: 'mysite'
		}
```

(Default) The document root for the webserver. The default value is "/var/www"
```
	nginx_site_removal_web_home: "/var/www"
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

	- hosts: your_webserver
	  vars_files:
	    - vars/main.yml
	  roles:
	    - stancel.nginx_site_removal 

or just pass the variables in the playbook

	- hosts: your_webserver 
	  vars:
		nginx_site_removal_sites_to_remove:
		  - {
			  url: 'mysite.com',
			  name: 'mysite'
			}
	  roles:
	    - stancel.nginx_site_removal

License
-------

GPLv3

Author Information
------------------

[Brad Stance](https://github.com/stancel)


