# cloudinit-ansible-multipass-demo Repository

This repository contains an demo Ansible playbook and cloudinit to demonstrate using both technologies hand in hand.

This uses [Multipass](https://multipass.run/) to spin up a slimline ubuntu image with a small [Cloudinit](https://cloudinit.readthedocs.io/en/latest/index.html) userdata file.

This Cloudinit file installs [ansible](https://docs.ansible.com/ansible/latest/getting_started/index.html) and then runs ansible-pull to pull down the playbook.yml file and runs it.

The playbook.yml sets up some basic ufw rules as a demo but this playbook could run much more of course.

## Getting Started

To get started with this repository, follow the steps below:

1. Clone the repository to your local machine:

   ```shell
   git clone https://github.com/mikedixson/cloudinit-ansible-multipass-demo.git
2. Run multipass:

   ```shell
   cd cloudinit-ansible-multipass-demo
   multipass launch --cloud-init userdata.yml
3. Connect to a shell in the container and check ufw rules
   ```shell
   multipass shell <name-of-container>
   sudo cat /etc/ufw/user.rules
