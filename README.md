# ansible-role-prowlarr

=========

Ansible Role to install prowlarr, an index manager/proxy for integration with various PVR apps.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `prowlarr_user`       | prowlarr | The primary user to run prowlarr  |
| `prowlarr_uid`        | *optional* | Commented out by default |
| `prowlarr_group`      | media | The primary group for `prowlarr_user` |
| `prowlarr_group_gid`  | *optional* | Commented out by default |
| `prowlarr_base_install_dir` | /opt | Base Install directory for prowlarr |
| `prowlarr_config_dir` |  /opt/data/prowlarr | Data directory to store configuration |
| `prowlarr_download_url` | https://prowlarr.servarr.com/v1/update/develop/updatefile?os=linux&runtime=netcore&arch=x64 | Link to the latest release |
| `prowlarr_port` | 9696 | Port in which prowlarr operates on, to add to Firewalld |
| `prowlarr_packages` |   ```- curl```  ```- sqlite``` | List of Packages Required to install and run prowlarr |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: prowlarr_servers
      roles:
        - aaron-cole.ansible_role_prowlarr


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole


