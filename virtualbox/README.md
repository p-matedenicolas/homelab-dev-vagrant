# Virtualbox development homelab

Vagrantfile used to deploy virtual machines in virtualbox to use as homelab

## Setup

There is an ssh directory for ease of use, just set the public key there to ssh into the machines

There is an [example config file](config.yaml.example) you can rename to ```config.yaml``` and adapt to your needs

The following variables can be configured

- user: name of the user to create in the box
- sshKeyHostPath: path to the ssh key to copy from the host
- sshKeyBoxPath: path to the ssh key to copy inside the box
- networkType: accepts `private_network` and `public_network` for the kind of network to use
- machines
    - The type and number of machines to be deployed
    - variables:
        - number: number of VMs of the current type to deploy
        - cpu: number of cpus to use by the VM
        - mem: RAM memory to use by the VM
        - box: name of the box in [Vagrant Cloud](https://app.vagrantup.com/boxes/search)
        - ip_base: base of the ip to assign to the VM
        - ip_start: this will be the last section of the ip to assign to the VM, it increases with each machine deployed, defined by the number variable
