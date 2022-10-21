PostgresSQL Debian 11
=========

Role to install PostgresSQL on Debian 11

Requirements
------------

This role requires root access.

Role Variables
--------------

PostgreSQL version:

    postgresql_version: 14

Superuser:

    postgresql_root_user: "root"

Superuser password:

    postgresql_root_password: "r00tPa55"

Option to only listen local, if set to false will listen on '*':

    listen_local: false

PostgreSQL locales that wil be generated for use by database:

    postgresql_locales:
      - 'en_US.UTF-8'

PostgreSQL users that will be added:

    postgresql_users:
      - user: bob # Required if adding users
        password: abc123
      - user: jane

Dependencies
------------

N/A

Example Playbook
----------------

    - hosts: pg_dbs
      roles:
         - abeardeddev.postgres

License
-------

MIT
