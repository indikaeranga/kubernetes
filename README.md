# kubernetes & containerD install using ansible

This ansible playbook write for install containerd and kubernetes lates versions. The system should meet the requirements for install. Please check this article for get idea of requirements. The official kubernetes and containerd documents can follow for more details if you wish to learn more.

https://ceylondevdb.blogspot.com/2023/04/install-containerd-runtime-and-setup.html

*** you should have atleast beginner knowledge for execute the ansible playbook. First, Add the host details to inventory file or ansible hosts file directly. After that, check ping and verify host and check syntax erros on playbook. Finally, execute the playbook.

1) download the playbook to your local server. (It should install ansible) 
2) vi /etc/ansible/hosts #open file for edit. add host details
[server]
192.168.126.110  #This should change according to your remote server details. you can add user/pass here if you want. Please check internet for that entry.
3) ansible -m ping server #Ping host for verify 
4) ansible-playbook containerd-kubernetes-install.yml --syntax-check #Verify playbook
5) ansible-playbook containerd-kubernetes-install.yml -v #Execute the playbook on remote verver. -v gives readable output
