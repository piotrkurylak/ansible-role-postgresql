## Role Name: Postgresql

Ansible role for installing postgresql on Debian distro systems.

## Requirements

None.

## Role Variables

Postgresql repository URL depending on distro. 
````yaml
postgresql_repo_url: "deb http://apt.postgresql.org/pub/repos/apt {{ ansible_distribution_release }}-pgdg main"
````

Postgresql repository signing key.
````yaml
postgresql_apt_key: "https://www.postgresql.org/media/keys/ACCC4CF8.asc"

````

Postgresql version. If you want a specific version, use 'postgresql-14'.
# By default this installs the latest version.
````yaml
postgresql_version: "postgresql"
````


## Dependencies

None.

## Example Playbook

````yaml
    - hosts: all
      become: yes
      roles:
         - postgresql
````

## License

MIT / BSD

## Author Information

Role created by Piotr Kurylak.