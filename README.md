Ansible Postgresql Role
=======================

An ansible role for installing and configuring Postgresql client / server

Role Variables
--------------

```yaml
postgresql_pgdg_repo: define if you wish to setup the PostgreSQL Global Development Group (PGDG) APT repository
postgresql_server_install: define if you wish to install postgresql server
postgresql_client_install: define if you wish to install postgresql client
postgresql_pkg_version: define the postgresql version
postgresql_extensions: define list of extension packages to install
postgresql_ext_postgis_pkg_version: define version of postgis if used
postgresql_data_directory: define postgres data directory path
postgresql_admin_user: define postgres user
postgresql_cluster_name: define cluster name
postgresql_cluster_reset: define if you want to reset the pg cluster
postgresql_locale: define default locale
postgresql_encoding: define default encoding
postgresql_conf_directory: define postgres configuration directory path
postgresql_service_state: define if the postgresql services needs to be running
postgresql_service_enabled: define if the postgresql service needs to be enabled
postgresql_conf: define a dictionary that holds your postgres configuration
postgresql_hba_conf: define your hba configuration
postgresql_additional_confs: define list of additional configuration files
```

Example Playbook
-------------------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.postgresql, become: true }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>
