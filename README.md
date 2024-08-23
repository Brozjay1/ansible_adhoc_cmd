PROJECT RECAP
  Using Ansible Adhoc command to automate the installation of Ngnix on target nodes from the control node 
- I launched EC2 instances and installed Ansible
- I created an inventory file on the control node
- I ping the inventory file to the check the connection of the target node [ansible webservers -i hosts.ini -m ping]
- I used it to install and configure Nginx on those instances. [ansible webservers -i hosts.ini -m ansible.builtin.apt -a "name=nginx state=present" --become]
- I enable and start the sucessfully install Ngnix. [ansible webservers -i hosts.ini -a 'systemctl enable nginx'/'systemctl start ngnix' --become]
- I verified the installation by accessing Nginx through a web browser through the public ip of the instances
- This project demonstrates how powerful and efficient Ansible can be for automating server configuration and management tasks.
