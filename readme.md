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

## Other Distributions

You can run this on other distributions. Please refer to the Ansible [documentation](https://docs.ansible.com/) for that

## Local

You can still run this project locally using [Docker](https://docker.com)

First you'll need to create the enviornment files containing the database secrets:

```bash
mkdir .env/
touch .env/mysql.env .env/phpmyadmin.env .env/wordpress.env
```

Here is an example of the values you'll need to fill in those files:

```env
# mysql.env
MYSQL_ROOT_PASSWORD=test
MYSQL_PASSWORD=test
MYSQL_USER=test
MYSQL_DATABASE=test

# phpmyadmin.env
MYSQL_ROOT_PASSWORD=cloud-1

# wordpress.env
WORDPRESS_DB_HOST=mysql
WORDPRESS_DB_USER=cloud-1
WORDPRESS_DB_PASSWORD=cloud-1
WORDPRESS_DB_NAME=cloud-1
```

And then you are ready to start the containers

```bash
docker compose up --build -d
```
