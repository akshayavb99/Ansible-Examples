# Setting up a Hadoop Cluster using Ansible Playbooks
### About the files
- <b>all_plays.yml</b> - Playbook used to execute a list of playbooks (install_hadoop.yml, setup_namenode.yml, setup_datanode.yml, start_services.yml)
- <b>hosts.txt</b> - Sample inventory file. Contains the details of each host under each group (hadoop_namenodes, hadoop_datanodes)
- <b>install_hadoop.yml</b> - Playbook to install Hadoop and the supporting JDK package.
- <b>setup_namenode.yml</b> - Playbook to configure the namenode.
- <b>setup_datanode.yml</b> - Playbook to configure the datanode(s).
- <b>start_services.yml</b> - Playbook to start the Hadoop service in namenode and datanode(s)
- <b>sample-dn-hdfs-site.xml.j2</b> - Jinja2 template file for the hdfs-site.xml file of the datanode(s).
- <b>sample-dn-core-site.xml.j2</b> - Jinja2 template file for the core-site.xml file of the datanode(s).
- <b>sample-nn-hdfs-site.xml.j2</b> - Jinja2 template file for the hdfs-site.xml file of the namenode.
- <b>sample-nn-core-site.xml.j2</b> - Jinja2 template file for the core-site.xml file of the namenode.<br><br>

### About the directories 
- <b>group_vars</b> - Directory containing the files which store the variables for each group (hadoop_namenodes, hadoop_datanodes)
