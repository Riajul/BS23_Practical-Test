# Conf Ansible Playbook for K8s
At first install ansible from control server

**To configure password less conf in master and worker nodes**
Run this from master server
> ssh-keygen
Copy the content *id_rsa.pub* from ~/.ssh/
Switch to the worker node and run *ssh-keygen*.
After that paste the content of public key of master server in worker nodes.
Go to ~/.ssh/ and create *authorized_keys* and paste there the contents.

Give password only for the first time, after that it will be password less ssh login.

**Ansible conf and Playbook**
Go to *ansible.cfg* and comment out *inventory      = /etc/ansible/hosts*
then got to *hosts* file add the master and worker node in like below:
>[anyname]
>hostname ansible_host=192.168.1.3

Run below command to check after adding if all nodes could be login by ansible:
>ansible -m ping all
it will give you success message

Run below ymls to configure Cluster

Run below command to check if your syntax is OK
>ansible-playbook serverprep.yml --syntax-check

Run below yml for Server Preparation:
>ansible-playbook serverprep.yml

After preparing the server,
run below to configure the Masternode:
>ansible-playbook masternodeconf.yml

When the master node ready prepare the Worker node:
>ansible-playbook workernodeconf.yml

To get the Dashboard, Metric Server and Service Account With RBAC:
>ansible-playbook dashboard_metricserver_svcrbac.yml
