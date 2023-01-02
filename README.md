# Ansible-Docker

**Project purpose**: 

This project uses ansible (server automation tool) to install docker and run docker images inside different droplets. 

**Hosts file**: 

Inside this file you need to specify your managed remote nodes, to define the server you need to specify either the hostname or the IP of the node. 

**Note**: 

Ansible also gives you the flexibility to create a custom inventory file at your preferred location on your control node to suit your preferences.

**Testing the default inventory:**

Before running the config file you need to test if the servers are accessible from your remote machine, you can perform this test using the following command 

 * Ansible all -i hosts -m ping 


**The YAML file (docker.yaml): 
**

The file has 2 plays: 

	1. The first play is used for installing docker and docker-compose inside the target node.
	2. The second play starts the dockers service and pull the image from its registry (redis image).
	

To run the play book you need to run the following command: 

* Ansible-playbook  -I hosts [file_name.yaml] 


**Reference**: 

https://docs.ansible.com/ansible/latest/collections/community/docker/docsite/scenario_guide.html![image](https://user-images.githubusercontent.com/11373339/210270679-3b2d1a2d-317a-4214-b13d-990ae96b7039.png)
