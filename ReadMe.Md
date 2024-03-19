#Ansible Topics
 Create a Bastion Host Ubuntu 20.04 LTS
Setup_Lab

1.Install Ansible & Terraform :
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt update
    sudo apt install ansible

    Terraform:

    wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
    echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
    sudo apt update && sudo apt install terraform

2. Run the Terraform scripts which generated the inv file.


3. Init the configuration file.
    ansible-config init --disabled > ansible.cfg
4. Open config files and make below changes
    a. Change the inv path /home/ubuntu/ansible-kelly
        inventory=/home/ubuntu/ansible-kelly
    b.change remote user
        remote_user=ubuntu
    c. Remote Hostchecking
        host_key_checking=False
    d. Add private key path
        private_key_file=/etc/ansible/ansiblekey.pem
    e. Copy the pemfile to the server through winscp or scp

5. Test out the connectivity
--------------------------
1.Adhoc commands
2. with_items for running iterations.
3. when condition
4. return code using rc
5. Ansible facts using Redis.
6. Copy, File, No_Log, Debug
7. Verbosity using -vvvv
8. Notify & Handlers
9. ignore_errors: true
10. block, rescue & always
11. Vault Encrypt String and File for aws_creds
12. shell & command modules
13. become_user
14. get_url and unarchive modules in redis playbook.
15. serial option select how many machine can run at a time. serial 1 will run
    on   one machine only.
16. lineinfile
17. Docker Swarm Configuration
18. Set-fact
19. --extra-vars ansible_user='ubuntu'
20. fetch
21. tags
22. Jinja Templates
23. Pre & Post Tasks
24. Roles and Ansible Galaxy
25. Dynamic Inventory
26. AWX
$Env:AWS_ACCESS_KEY_ID="XX"
$Env:AWS_SECRET_ACCESS_KEY="XXX"
$Env:AWS_REGION="us-east-1"


