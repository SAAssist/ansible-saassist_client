Role Name
=========

This roles helps to install Security APAR Assistant Client (saassist-client)
across IBM AIX and PowerVM (VIOS).

Requirements
------------

This role requires Ansible 2.4 or higher that users aix_lvol


Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows:

    saassist_path: /opt/saassist/saassist-client  # path for saassist-client and Logical Volume
    saassist_tmp: /opt/saassist/tmp               # temp dir
    saassist_protocol: http                       # http or nfs
    saassist_server: "0.0.0.0"                    # Security APAR Assistant Server
    saassist_server_http_port: 8000               # http port (when http protocol is used)
    saassist_server_nfs_fs: /opt/saassist/saassist-server/data/repos    # NFS File System is used
    saassist_client_file: /srv/myfiles/saassist-client-0.2.0.zip        # Last version of saassist-client package


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: saassist }

License
-------

BSD

Author Information
------------------

Kairo Araujo