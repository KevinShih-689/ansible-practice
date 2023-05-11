# ansible-practice
###### 🚀 To practice how to write ansible playbook.
## Directory Layout
```
ansible-practice/
├── inventories/
│   ├── production/
│   │   ├── hosts
│   │   └── group_vars/
│   └── staging/
│       ├── hosts
│       └── group_vars/
├── roles/
│   ├── common/
│   │   ├── tasks/
│   │   ├── handlers/
│   │   ├── files/
│   │   ├── defaults/
│   │   ├── templates/
│   │   └── vars/
│   │       ├── main.yml
│   │       └── more.yml
│   └── webserver/
│       ├── tasks/
│       ├── files/
│       └── templates/
├── site.yml ( Master Playbook )
├── deploy-webserver.yml
├── provision-infrastructure.yml
├── production.yml
├── staging.yml
└── ansible.cfg
```
## Before you start
##### ⚡ Remember to share your controller ssh public key `id_rsa.pub` with the worker node you want to control.
```
ℹ️ The list of worker nodes will store in inventories folder
```
### Sharing Controller public key
1. #### Generate ssh key in Controller
    ```shell=
    $ ssh key-keygen
    ```
2. #### Copy public key to worker node
    ###### Controller
    ```shell=
    $ cat ./.ssh/id_rsa.pub
    ssh-rsa XXXXXXXXXXXX...
    ```
    ###### Worker Node
    ```shell=
    $ vi ./.ssh/authorized_keys
    ```

## Playbook
```
ℹ️ Remember to execute the ansible command in the project's root directory.
```
Name   |   Description  | roles
-------|-------------|---------
test-playbook | Test to ping managed node | ping-sample
install-docker-playbook | Install Docker | docker-installer</br>pip-installer
## Virtual Machine
* #### Control Node
    
* #### Managed Node
    * ##### RHCSAPrac
        * ###### RHEL 8
        * ###### IP: 10.250.75.112
    * ##### RockyLinux
        * ###### Rocky Linux 8.7
        * ###### IP: 10.250.75.116
## VS Code Tools
* ##### [Ansible](https://marketplace.visualstudio.com/items?itemName=redhat.ansible)
* ##### [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
* ##### [Jinja](https://marketplace.visualstudio.com/items?itemName=wholroyd.jinja)
* ##### [SFTP](https://marketplace.visualstudio.com/items?itemName=Natizyskunk.sftp) ( OPTIONAL )
## Reference
* ###### [Ansible Best Practices](https://github.com/ansible/ansible-examples)
* ###### [Study Notes](https://hackmd.io/@KevinShihYC/ryafhGqYv)
* ###### [Ansible Best Practice](https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html)
* ###### [Ansible Doc](https://docs.ansible.com/ansible/latest/index.html)
* ###### [Sample Project](https://github.com/tsoliangwu0130/my-ansible/blob/master/docker-jenkins.yml)
* ###### [Sample Introduction](https://tso-liang-wu.gitbook.io/learn-ansible-and-jenkins-in-30-days/ansible/ansible)

![Alt](https://repobeats.axiom.co/api/embed/4a0d48eb8f795a92130598c7ebef46a7ad237871.svg "Repobeats analytics image")
