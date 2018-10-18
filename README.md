[![GoKEV](http://GoKEV.com/GoKEV200.png)](http://GoKEV.com/)

<div style="position: absolute; top: 40px; left: 200px;">

# GoKEV-lab-provisioner

This project is an Ansible role to deploy one or many EC2 instances for lab purposes
  - This role assumes you're feeding credentials through an Ansible Tower credential type


## Example Playbooks
Here's an example of how you could launch this role


<pre>---
- name: Back up a system with GoKEV-lab-provisioner
  hosts: servers-to-backup

  roles:
    - GoKEV.lab-provisioner

</pre>

## With a requirements.yml that looks as such:

<pre>
---
- name: GoKEV.lab-provisioner
  version: master
  src: https://github.com/GoKEV/GoKEV-lab-provisioner.git
</pre>


## Troubleshooting & Improvements

- Not enough testing yet

## Notes

  - Not enough testing yet

## Author

This project was created in 2018 by [Kevin Holmes](http://GoKEV.com/).


