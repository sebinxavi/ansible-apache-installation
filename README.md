# Ansible script for Installing Apache & Hosting a Simple Website

This Ansible Script will helps to Install Apache and Host a Simple Website. Ansible is an open source IT Configuration Management, Deployment & Orchestration tool. It aims to provide large productivity gains to a wide variety of automation challenges.

## Features of Terraform

- Infrastructure Provisioning
- Configuration Management
- IT automation
- Continuous deployment
- Application Development
- Network Automation
- Security Automation
- Infrastructure Orchestration 

## Prerequisites
- Ansible version - 2.9
- Linux operating System
- SSH PEM key for Remote Servers
- SSH User with sudo privilege

## _Usage_

This script will perform following operations;

- Install Apache
- Download and Unzip the website content to Remote Host
- Copy Website files to Apache document root
- Restart Apache

## Ansible Installation

```sh
$ yum -y install ansible
```

## How to configure

With Ansible installed, you are ready to provision the remote server by following the below steps.

```sh
$ git clone https://github.com/sebinxavi/ansible-apache-installation.git
$ cd ansible-apache-installation
```

Open the file 'hosts' and edit the Remote hosts details

The Sample format is provided below,

```sh
[ubuntu]
172.31.43.55  ansible_user=ec2-user ansible_port=22 ansible_ssh_private_key_file="ubuntu.pem"
```

- Add a Group name for the remote hosts. Example: ubuntu
- Add the Remote Host IP address. Example: 172.31.43.55
- Add the Remote SSH User. Example: ec2-user
- Add the SSH port number: Example: 22
- Import the SSH key file to the same location in which we are going to run the Ansible playbook and add the key name to the file hosts

Run the ansible-playbook from the master server by below command,

```sh
$ ansible-playbook -i hosts apache.yml
```

## Results

Access the IP address of the Remote Host server in Brower and you can see the sample website.
