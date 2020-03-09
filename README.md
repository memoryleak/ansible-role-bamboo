memoryleak.bamboo
=================

Installs and configures Bamboo

Requirements
------------

In order for Bamboo to run you need to have Java installed and configured.

Role Variables
--------------

  bamboo_version: # Bamboo version to isntall
  bamboo_copy_from_file: # If you prefer to copy over the installation tarball provide the path here
  bamboo_install_prefix: # Parent installation folder
  bamboo_home_path: # Path to Bamboo's home folder
  bamboo_reverse_proxy_port: # If Bamboo is behind a proxy server, provide port here.
  bamboo_reverse_proxy_domain: # If Bamboo is behind a proxy server, provide URL here.
  bamboo_user: # The user the process should run as
  bamboo_group: # The group the process should run as
  bamboo_create_systemd: # Creates a systemd service entry
  bamboo_jvm_memory: # JVM memory settings
    minimum: 1G
    maximum: 12G

Dependencies
------------

Recommended: A Java role.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: memoryleak.bamboo }

License
-------

MIT

Author Information
------------------

Haydar Ciftci