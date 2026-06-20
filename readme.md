# Could-1

This project is about auto deployment and configuration of environments. It uses [Ansible](https://github.com/ansible/ansible) for this job.

## How to run ?

 > __*NOTE:*__ Before running this project you'll need the private ssh key of the server in order to run the ansible playbook.

 ```bash
 cd /path/to/project
 mkdir .ssh
 cp /path/to/cloud-1.pem /path/to/project/.ssh
 ```
 
Using Nix:

```bash
nix develop
```

You can run this on other distributions. Please refer to the Ansible [documentation](https://docs.ansible.com/) for that
