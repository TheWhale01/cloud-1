# Could-1

This project is about auto deployment and configuration of environments. It uses [Ansible](https://github.com/ansible/ansible) for this job.

## How to run ?

Using Nix:

```bash
nix develop
```

You can run this on other distributions. Please refer to the Ansible [documentation](https://docs.ansible.com/) for that

## Commands
Connect to AWS : ssh -i ~/.ssh/cloud-1.pem ubuntu@16.171.46.109
Verify your inventory ansible-inventory:  -i inventory.ini --list
