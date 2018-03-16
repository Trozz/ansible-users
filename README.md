Role Name
=========

This role pulls a git repository that is filled with json files, it will create the users within the files and has a field within the json for enabled or disabled to create/remove accounts

Requirements
------------

None - local machine requires git

Role Variables
--------------

git_user: <username for github>
git_token: <access token for github>
user_keys: <local path to clone repo>
home_dir: <remote home directory>
git_repo: <github repo ending in .git>


Dependencies
------------

None

Example Playbook
----------------

```
- hosts: servers
  vars:
    git_user: wade_wilson
    git_token: mysuperuniquegeneratedtoken
    user_keys: /tmp/users
    home_dir: /home/
    git_repo: trozz/ssh-keys.git
  roles:
     - { role: trozz.ansible-users }
```
License
-------

BSD

Author Information
------------------

Trozz <www.trozzy.net>
