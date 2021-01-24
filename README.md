# Ansible-Examples
## Welcome!!<br>
This repository contains all the Playbooks and other files used to work with different applications for Ansible. Each example is summarized below, and for more details on how to work on these examples yourseld, please go to the respective example's directory present in the main repository.<br>

## Pre-requisites<br>
1.Ensure that you have Ansible installed on the system you are using as the controller node. For details on the installation, please refer to [the official installation guide provided by Ansible.](https://docs.ansible.com/ansible/latest/installation_guide/index.html)<br><br>
2. Ensure that you have installed sshpass on the controller node, so that the controller can use the ssh connection to the host node(s) with password. For more details on the installation, please refer to [this guide.](https://www.tecmint.com/sshpass-non-interactive-ssh-login-shell-script-ssh-password/#:~:text=Install%20sshpass%20on%20Linux%20Systems%20In%20RedHat%2FCentOS%20based,can%20install%20it%20using%20apt-get%20command%20as%20shown.)<br><br>
3. Setup the configuration file and the Inventory and check for connectivity between the controller and target nodes(s) as directed in the [setup-examples directory](https://github.com/akshayavb99/Ansible-Examples/tree/main/setup-samples)

-----
 
## Examples
### [Setting up the YUM repository and Docker Community Edition in RHEL8](https://github.com/akshayavb99/Ansible-Examples/tree/main/docker-webserver)
In this example, we will be looking at how we can configure the YUM repository and set up Docker Community Edition in RHEL8 using Ansible Playbooks and basic Linux scripting.<br>
Detailed explanation: https://akshayavb99.medium.com/automation-with-ansible-common-terms-and-setting-up-docker-7a689c4fa8bb <br>

### [Setting up a Hadoop Cluster](https://github.com/akshayavb99/Ansible-Examples/tree/main/setup-hadoop)
In this example, we will be looking at how we can set up a Hadoop cluster using Ansible Playbooks and basic Linux scripting.<br>
Detailed explanation:<br> https://akshayavb99.medium.com/automation-with-ansible-setting-up-hadoop-clusters-58bc47e5496d <br>

### [Setting up backend webservers with HAProxy Loadbalancer](https://github.com/akshayavb99/Ansible-Examples/tree/main/setup-haproxy)
In this example, we will be looking at how we can set up a loadbalancer for webservers using Ansible Playbooks.<br>
