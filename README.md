# tf_os_k8s
Tunsten Fabric &amp; Openstack &amp; K8s Integration.
1. git clone https://github.com/xiaoruiguo/tf-ansible-deployer.git
2. vagrant@ubuntu-bionic:~$ sudo passwd root
3. vagrant@ubuntu-bionic:~$ su - root
4. root@ubuntu-bionic:~# ssh-keygen -t rsa 
5. root@ubuntu-bionic:~# vi /etc/ssh/sshd_config
   PasswordAuthentication yes 
   PasswordAuthentication yes  
6. root@ubuntu-bionic:~# systemctl restart ssh
7. root@ubuntu-bionic:~# uname -a
   Linux ubuntu-bionic 4.15.0-54-generic #58-Ubuntu SMP Mon Jun 24 10:55:24 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux
8. mkdir -p /etc/docker
9.  vagrant@ubuntu-bionic:~$ cd tf-ansible-deployer/
10. cp etc/docker/daemon.json /etc/docker/
11. systemctl daemon-reload
12. systemctl daemon-reload
13. systemctl restart docker
14. vagrant@ubuntu-bionic:~/tf-ansible-deployer$ sudo apt-get install sshpass python-pip -y
15. vagrant@ubuntu-bionic:~/tf-ansible-deployer$ pip install --upgrade pip==20.2.2
16. vagrant@ubuntu-bionic:~/tf-ansible-deployer$ pip install pyyaml requests
17. vagrant@ubuntu-bionic:~/tf-ansible-deployer$ pip install ansible==2.7.18
18. vagrant@ubuntu-bionic:~/tf-ansible-deployer$ ansible-playbook -i inventory/ -e orchestrator=openstack playbooks/configure_instances.yml
19. ansible-playbook -i inventory/ -e orchestrator=openstack playbooks/install_openstack.yml  -v -v.
