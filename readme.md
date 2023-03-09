Author - Meenu Agrawal

About the Ansible:

Ansible is simple open source IT engine which automates application deployment, intra service orchestration, cloud provisioning and many other IT tools.
Ansible is easy to deploy because it does not use any agents or custom security infrastructure.
Ansible uses playbook to describe automation jobs, and playbook uses very simple language i.e. YAML (It’s a human-readable data serialization language & is commonly used for configuration files, but could be used in many applications where data is being stored)which is very easy for humans to understand, read and write. Hence the advantage is that even the IT infrastructure support guys can read and understand the playbook and debug if needed (YAML – It is in human readable form).

How Ansible Works?
The picture given below shows the working of Ansible.
Ansible works by connecting to your nodes and pushing out small programs, called "Ansible modules" to them. Ansible then executes these modules (over SSH by default), and removes them when finished. Your library of modules can reside on any machine, and there are no servers, daemons, or databases required.
 
The management node in the above picture is the controlling node (managing node) which controls the entire execution of the playbook. It’s the node from which you are running the installation. The inventory file provides the list of hosts where the Ansible modules needs to be run and the management node does a SSH connection and executes the small modules on the hosts machine and installs the product/software.

How to install Ansible:

For installing Ansible you have to configure PPA on your machine. For this, you have to run the following line of code −

       $ sudo yum update 
       $ sudo yum install software-properties-common 
       $ yum install epel*
       $ yum install ansible -y
       $ ansible --version
    
      Note: Please make sure python is installed or not. If it is not installed first install python then follow above steps. 

After running the above line of code, you are ready to manage remote machines through Ansible. Just run Ansible–version to check the version and just to check whether Ansible was installed properly or not.

Ansible folder explanation :


1.	default folder:- variables will be used across the application.
       2.   secret folder:-  all credentials username and password will be inside this folder which    will be encrypted.
       3.   environment folder:- Specific environment related variables will be there.
       4.   Data folder:- All environment related data.
       5.   roles :- All roles will be in this folder.
6.	file folder:- It contains all .conf data.
       7.   template:- Similar to file, template contains dynamic data.
