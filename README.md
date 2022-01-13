# Project-1
The files in this repository were used to configure the network depicted below.

TODO: Update the path with the name of your diagram

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

_TODO: elk-playbook.yaml
This document contains the following details:

Description of the Topologu
Access Policies
ELK Configuration
Beats in Use
Machines Being Monitored
How to Use the Ansible Build
Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly _____, in addition to restricting _____ to the network.

TODO: What aspect of security do load balancers protect? What is the advantage of a jump box? Load balancers protects the system from DDoS attacks by shifting attack traffic. The advantage of a jump box is to give access to the user from a single node that can be secured and monitored. Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _____.
TODO: What does Filebeat watch for?
Filebeat watches for any information in the file system which has been changed and when it has.
TODO: What does Metricbeat record?
Metricbeat takes the metrics and statistics that collects and ships them to the output you specify The configuration details of each machine may be found below. Note: Use the Markdown Table Generator to add/remove values from the table.
Name	Function	IP Address	Operating System
Jump Box	Gateway	10.2.0.4	Linux
VM1	Server	10.2.0.7	Linux
VM2	Server	10.2.0.6	Linux
ELK	Server	10.4.0.4	Linux
Access Policies
The machines on the internal network are not exposed to the public Internet.

Only the _____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:

TODO: Add whitelisted IP addresses 99.153.201.34 Machines within the network can only be accessed by _____.
TODO: Which machine did you allow to access your ELK VM? What was its IP address? Jumpbox 10.2.0.4 A summary of the access policies in place can be found in the table below.
Name	Publicly Accessible	Allowed IP Addresses
Jump Box	Yes	
VM1/2	No	10.2.0.4
Elk.	No	10.2.0.6/10.2.07
Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...

TODO: What is the main advantage of automating configuration with Ansible? Advantage is that you can put commands into multiple servers from a single playbook
The playbook implements the following tasks:

TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc.
...Install: docker
... Install Python
Launch Docker Container elk
The following screenshot displays the result of running docker ps after successfully configuring the ELK instance.

TODO: Update the path with the name of your screenshot of docker ps output

Target Machines & Beats
This ELK server is configured to monitor the following machines:

TODO: List the IP addresses of the machines you are monitoring 10.2.0.6, 10.2.0.7 We have installed the following Beats on these machines:
TODO: Specify which Beats you successfully installed Filebeat and metric beat These Beats allow us to collect the following information from each machine:
TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., Winlogbeat collects Windows logs, which we use to track user logon events, etc. Filebeat collects the log data, metricbeat collects metrics and statistics.
Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:

SSH into the control node and follow the steps below:

Copy the _____ file to _____.
Update the _____ file to include...
Run the playbook, and navigate to ____ to check that the installation worked as expected.
TODO: Answer the following questions to fill in the blanks:

Which file is the playbook? Where do you copy it? /etc/ansible/file/filebeat-config.yaml

Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on? edit the /etc/ansible/host file to add webserver/elkserver ip addresses-

_Which URL do you navigate to in order to check that the ELK server is running? www.99.153.201.34:5601 As a Bonus, provide the specific commands the user will need to run to download the playbook, update the files, etc.%
ansible-playbook (playbook name)
