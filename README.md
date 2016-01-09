Role Name
=========

nginx_django_setup

Requirements
------------

Pre-created Django project over Ubuntu server.

Role Variables
--------------

nginx_dir: "/etc/nginx"  
nginx_conf_dir: "{{nginx_dir}}/sites-available"  
nginx_sites_dir: "{{nginx_dir}}/sites-enabled"  
nginx_access_log: "/home/{{project_name}}/logs/access.log"  
nginx_error_log: "/home/{{project_name}}/logs/error.log"  


Dependencies
------------

- { role: micropyramid.nginx }


Example Playbook
----------------

    - hosts: servers
      remote_user: root
      roles:
        - { role: micropyramid.nginx_django_setup, project_name: "your_project_name", server_name: "domain_name_or_ip_addr", server_port: "port_number" }


License
-------

MIT
