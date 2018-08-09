# Gluster_Ansible

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
![Fun: Extreme](https://img.shields.io/badge/fun-extreme-orange.svg)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![stability-experimental](https://img.shields.io/badge/stability-experimental-orange.svg)


Ansible playbook to deploy gluster



### How to use
- Create ansible vault.yml with your credential 

example:  vault.yml
```sh 
---
username: YOUR_USERNAME
password: YOUR_PASSWORD
```

To Create vault.yml execute
```sh
# ansible-vault create vault.yml
```

- Control node should have passwordless SSH to manage node

Generate SSH key if required and copy SSH public key to manage node
```sh
# ssh-keygen
# ssh-copy-id user@<manage_node_ip>
```

- Manage node should have a empty disk attach with name ```sdb```

- Make sure inventory is modified as required

- To run playbook
```sh
# ansible-playbook gluster1.yml --ask-vault-pass
```

## Licensing
Gluster_Ansible is licensed under GNU General Public License v3.0. See [LICENSE](https://github.com/khomesh24/gluster_ansible/blob/master/LICENSE/)
