### In this example, you can set up a Kubernetes cluster using AWS EC2 instances, and then setup MySQL and WordPress applications using pods launched on the K8s cluster. 
By default, we have set the counts as 1 Master Node and 2 Worker Nodes.

The main_setup.yml file consists of 4 major parts:
1. Provisioning EC2 instances for K8s master node and worker node(s). You can directly change the number of each type of nodes, as well as the tags of the EC2 instances. Ensure that you change the hosts values of subsequent plays in the file, as the AWS dynamic inventory groups the hosts according to the EC2 instance tags.
2. Configuring the K8s Master node.
3. Configuring the K8s worker node(s).
4. Setting up WordPress and MySQL pods and integrating them. There are variables like pod names, MySQL database authentication parameters like root password etc., which you can change in the vars/main.yml file of the setup-mysql-wp role.

To set the specifications of your AWS instances like AMI ID, AWS Secret Key etc., you can edit the vault file main.yml provided in the vars directory of the provision-ec2 role using the following command
```
ansible-vault edit <path>/k8scluster-setup/roles/provision-ec2/vars/main.yml --ask-vault-pass
```
The password for the vault is <b>redhat</b>.

After setting all of your specifications, ensure that your terminal knows where to look for your AWS credentials. For this you can do one of the following:
1. Export them on your terminal
```
export AWS_ACCESS_KEY=<YOUR ACCESS KEY>
export AWS_SECRET_KEY=<YOUR SECRET KEY>
```
2. Define the keys in inventory/ec2.ini file. This method is preferable as it helps avoid exporting the variables for every terminal we use. But ensure that the file is properly protected as your AWS credentials are sensitive.

Note that, we need a local copy of the private key we attach to the EC2 instance(s). Store it in the same location as the main_setup.yml file. The absolute path of the key must also be updated in the ansible.cfg file given. In this case, we have used only one key for all instances. The key must be in the .pem format.

Finally, once these have been completed, you can run the playbook using
```
ansible-playbook main_setup.yml --ask-vault-pass
```
The vault password here is asked to use the variables in the vars/main.yml file of the provision-ec2 role. So we can give the same password here.


