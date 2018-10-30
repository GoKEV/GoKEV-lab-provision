[![GoKEV](http://GoKEV.com/GoKEV200.png)](http://GoKEV.com/)

<div style="position: absolute; top: 40px; left: 200px;">

# GoKEV-lab-provision

This project is an Ansible role to deploy one or many EC2 instances for lab purposes
  - This role assumes you're feeding credentials through an Ansible Tower credential type


## Example Playbooks
Here's an example of how you could launch this role


<pre>
---
- name: Build an EC2 instance
  hosts: localhost
  gather_facts: no

  vars:
    user_sshkey: my-private-key
    user_instype: t2.small
    user_image: ami-26ebbc5c
    user_vpc: vpc-a12345678
    user_subnet: subnet-12345678
    user_secgrp: security-group-name
    user_awskey: ABCDEFGHIJKLMNOPQRST
    user_awssec: abcdefghijklmnopqrstuvwxyz0123456789
    user_region: us-east-1
    user_tags:
      Name: GoKEV EC2 Lab
      Event: Some Workshop Event
      Owner: GoKEV
      Contact: "kev@redhat.com"
      Application: AnsibleRED

  roles:
    - GoKEV-lab-provision

- hosts: newec2
  roles:
    - GoKEV-lab-installtower
    - GoKEV-lab-configtower

</pre>

## With a requirements.yml that looks as such:

<pre>
---
- name: GoKEV.lab-provision
  version: master
  src: https://github.com/GoKEV/GoKEV-lab-provision.git

- name: GoKEV.lab-installtower
  version: master
  src: https://github.com/GoKEV/GoKEV-lab-installtower.git

- name: GoKEV.lab-configtower
  version: master
  src: https://github.com/GoKEV/GoKEV-lab-configtower.git

</pre>


## Troubleshooting & Improvements

- Not enough testing yet

## Notes

  - Not enough testing yet

## Author

This project was created in 2018 by [Kevin Holmes](http://GoKEV.com/).


