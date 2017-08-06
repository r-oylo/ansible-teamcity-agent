TeamCity Agent
=========

This role will install and configure TeamCity Agent for TeamCity Server - CI tool from Jetbrains.

## Requirements
1. `teamcity-server` - TeamCity Server
2. `geerlingguy.java` - Java is required on TeamCity Agent

## Role Variables
| Variable name               | Default value      | Description                |
|-----------------------------|--------------------|----------------------------|
| teamcity_agent_server_url   |  `localhost`       | TeamCity Server URL        |
| teamcity_agent_server_port  |  `8111`            | TeamCity Server Port       |
| teamcity_agent_install_dir  |  `/opt/buildAgent` | TeamCity Agent Install Dir |
| teamcity_server_user_name   | `teamcity`         | Teamcity Adminin User      |
| teamcity_server_user_passwd | `teamcity`         | Teamcity Admin Password    |

## Dependencies
This role depends on `java` role.

## Example Playbook
Example playbook:

```yaml
- hosts: teamcity-agent
  roles:
    - matevarga.teamcity-agent
```

## Author Information
This role was originally created by Mateusz Trojak for [Brainly](http://www.brainly.com)
I have forked the role to make it more suitable for my own needs.

## License
Copyright © 2017 Mate Varga. See LICENSE for details.
