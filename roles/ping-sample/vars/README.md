# Vars
* ###### 用來放置變數
* ###### 優先度高於 ` /defaults/main.yml `
* ###### Ansible 預設讀取此目錄下的 ` main.yml `

##### 優先級 ( 高 到 低 )
1. ###### 使用 "-e" 參數在命令行中定義的變量
2. ###### role or playbook 會抓取 vars and defaults
3. ###### playbook 會抓取 playbook裡面定義的 var 
    ###### 定義在 Playbook，如下:
    ```
    - name: My Playbook
        hosts: all
        vars:
        my_var_1: value1
        my_var_2: value2
        tasks:
        - name: My Task
            debug:
            var: my_var_1
    ```
4. ###### 執行playbook的 hosts 裡面的 group_vars and host_vars
5. ###### 配置文件中的 Global vars

###### [Ansible Doc to introduction var](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable)
