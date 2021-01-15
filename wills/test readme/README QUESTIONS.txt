ADME.md
Automated ELK Stack Deployment
The files in this repository were used to configure the network depicted below.

TODO: Update the path with the name of your diagram

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the (YAML) file may be used to install only certain pieces of it, such as Filebeat.

Elk-Playbook.yml._
This document contains the following details:

Description of the Topolog
Access Policies
ELK Configuration
Beats in Use
Machines Being Monitored
How to Use the Ansible Build
Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly (dynamic), in addition to restricting (access) to the network.

(Question): "What aspect of security do load balancers protect?" 

A.) Load balancing is defined as the methodical and efficient distribution of network or application traffic across multiple servers in a server farm. Each load balancer sits between client devices and backend servers, receiving and then distributing incoming requests to any available server capable of fulfilling them. Load-balancers work on layers 4-7 of the OSI model .

(Question): "What is the advantage of a jump box?"

A.) Jump box prevents VM’s from being exposed to outside internet. The Jump Box is the main entryway to your server group. The Jump Box is 1st in line to Vm's preventing all VM's from being exposed to the public internet. Advantages of using a Jump box, it allows you turn it off to stop any (Remote Access)

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the (Configuration) and system (Files).

(Question): What does Filebeat watch for? 

A.) Filebeat watches log files that users specify, collects log events, and forwards them for indexing. 

(Question): What does Metricbeat record?

 A.) Metricbeat is a lightweight shipper that you can install on your servers to periodically collect metrics from the operating system and from services running on the server.

The configuration details of each machine may be found below. Note: Use the Markdown Table Generator to add/remove values from the table.

Name	Function	IP Address	Operating System
Jump Box	Gateway	10.0.0.1	Linux
Web-1	Web server	10.0.0.5	Linux
Web-2	Web server	10.0.0.6	Linux
ElkProject1VM	Web Server	10.1.0.4	Linux

Access Policies
The machines on the internal network are not exposed to the public Internet.

Only the (Jump Box Provisioner) machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:

(Question): Add whitelisted IP addresses 

A summary of the access policies in place can be found in the table below.

Name	Publicly Accessible	Allowed IP Addresses
Jump Box	Yes	10.0.0.1 10.0.0.2
Web-1	No	52.183.102.245
Web-2	No	52.183.102.245
ElkProject1VM	No	52.183.102.245
Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because..

A.) The use of Ansible allows for changes across all Vms 

(Question): What is the main advantage of automating configuration with Ansible? 

A.) Ansible does a great job of automating Docker and operationalizing the process of building and deploying containers. If you’re managing a traditional IT system, for example, it can be hard to add container-tooling functionality. But Ansible removes the need to do processes manually. There are four main advantages of using Ansible with Docker: 1. Portability/Flexibility

(Question): In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
Elk Instalation:) 

TODO: Update the path with the name of your screenshot of docker ps output

Target Machines & Beats
This ELK server is configured to monitor the following machines: 10.1.0.4 10.0.0.4 10.0.0.5 10.0.0.6

List the IP addresses of the machines you are monitoring_
We have installed the following Beats on these machines:

: Specify which Beats you successfully installed A.) Filebeat and MetricBeat
These Beats allow us to collect the following information from each machine:

(Question): In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., Winlogbeat collects Windows logs, which we use to track user logon events, etc. A.) Filebeat watches/monitors log files, log events and locations that users specify, Example: Inputs and harvesters A.) Metricbeat watches for any information in the file system which has been changed/altered and time frame. Takes the statistics
Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:

SSH into the control node and follow the steps below:

Copy the _____ file to _____.
Update the _____ file to include...
Run the playbook, and navigate to Jump box to check that the installation worked as expected.
TODO: Answer the following questions to fill in the blanks:

_Which file is the playbook? Where do you copy it? 

Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on? 

A.)
_Which URL do you navigate to in order to check that the ELK server is running? A.)http://[MYVM-ip]:5601/app/kibana
As a Bonus, provide the specific commands the user will need to run to download the playbook, update the files, etc.

© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
