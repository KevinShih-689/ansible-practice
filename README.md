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
├── workspace/
│   ├── deploy-webserver.yml
│   └── provision-infrastructure.yml
├── site.yml
├── production.yml
├── staging.yml
├── ansible.cfg
└── requirements.yml
```
## VS Code Tools
* ##### [Ansible](https://marketplace.visualstudio.com/items?itemName=redhat.ansible)
* ##### [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
* ##### [Jinja](https://marketplace.visualstudio.com/items?itemName=wholroyd.jinja)
* ##### [SFTP](https://marketplace.visualstudio.com/items?itemName=Natizyskunk.sftp) ( OPTIONAL )
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

## Reference
* ###### [Ansible Best Practices](https://github.com/ansible/ansible-examples)
* ###### [Study Notes](https://hackmd.io/@KevinShihYC/ryafhGqYv)
* ###### [Ansible Best Practice](https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html)
* ###### [Ansible Doc](https://docs.ansible.com/ansible/latest/index.html)

![Alt](https://repobeats.axiom.co/api/embed/4a0d48eb8f795a92130598c7ebef46a7ad237871.svg "Repobeats analytics image")
