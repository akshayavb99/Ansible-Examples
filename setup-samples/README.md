## Setup-Examples
This directory contains samples for the Ansible configuration file and the inventory. You can modify it as per your requirements. Note that it is best to place these files in your current Ansible Workspace

To ensure your controller node and target node(s) can communicate with each other, use the following command
```
ansible all -m ping
```
If it is successful, then you will get an output similar to the one shown in the image below.


