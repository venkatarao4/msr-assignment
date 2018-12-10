This is the below procedure I follow for assignment

## Prerequisites

I have installed below software in my laptop and it is ansible controller

* Ansible
* Awscli
* Boto
* Boto3
* Openssh-server

Testing my PC, if all are working fine

`ansible –version`

`awscli --version`

## Execution Procedure

Now, I have created a folder name “msr-assignment”

All the code will be inside msr-assignment folder

### First Question

This script will create ec2 instances in AWS

`ansible-playbook one.yml`

Now once this is executed goto aws console and copy the public ip address of all the servers that are created
There will file “inventory.txt”, update it those ip address

### Second Question

This Script will install the softwares given in second question to the above servers

`ansible-playbook –i inventory.txt two.yml`

### Third Question

This script will install docker “httpd” image from dockerhub and copy the “index.html” page and start container

`ansible-playbook –i inventory.txt three.yml`

### Fourth Question

This script will install docker “couchdb” image from dockerhub and start the container

`ansible-playbook –i inventory.txt four.yml`

### References

These are some links i have refereed to get the package names and right docker container

`https://docs.ansible.com/ansible/2.5/modules/docker_container_module.html`

`https://hub.docker.com/_/httpd/`

`https://hub.docker.com/_/couchdb/`


