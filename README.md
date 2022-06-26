# zerodimensional.space

Automatically deploys an instance of [zerodimensional.space](zerodimensional.space).

## Prerequisites

- RHEL8
- Copr module for Ansible. Install with:

  `ansible-galaxy collection install community.general`
- DNS configured for zerodimensional.space.
- Ansible `/etc/ansible/hosts` configured. Example:

  `zerodimensional.space  ansible_ssh_private_key_file=$PRIVATE_KEY`
  
## Usage

`ansible-playbook site.yml`

## Website Configuration

Caddyfile is located at `roles/common/files/Caddyfile`.

Any changes in the website subdirectories of `roles/common/files/` will be propagated to the live server.

## Todo

- [ ] Automatically provision an AWS EC2 instance if none already exists.
