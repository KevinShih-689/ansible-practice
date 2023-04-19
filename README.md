# ansible-practice
###### To practice how to write ansible playbook.
## Official Document
* ###### [Follow this link](https://docs.ansible.com/ansible/latest/getting_started/index.html)
## Project Architechture
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
│   │   ├── files/
│   │   └── templates/
│   ├── webserver/
│   │   ├── tasks/
│   │   ├── files/
│   │   └── templates/
│   └── database/
│       ├── tasks/
│       ├── files/
│       └── templates/
├── site.yml
├── production.yml
├── staging.yml
├── ansible.cfg
└── requirements.yml
```
## Study Notes
* ###### [HackMD](https://hackmd.io/@KevinShihYC/ryafhGqYv)
