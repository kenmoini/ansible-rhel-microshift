# ansible-rhel-microshift

A simple Playbook that will set up a RHEL 9 host to run Microshift.

## Create a Libvirt VM

```bash
ansible-playbook -e mode=create
```

Just wait for the VMs to shut down, then start them back up, and subscribe them.

## Deploy Microshift

```bash
# Install needed collections/roles
ansible-galaxy collection install community.general
ansible-galaxy collection install ansible.posix

# Run the playbook
ansible-playbook -i .generated/gen_inventory deploy-microshift.yml
```
