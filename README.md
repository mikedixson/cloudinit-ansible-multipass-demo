# cloudinit-ansible-multipass-demo Repository

This repository contains an demo Ansible playbook and cloudinit to demonstrate using both technologies hand in hand.

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
