# Vars
* ###### 用來放置變數
* ###### 優先度高於 ` /defaults/main.yml `
* ###### Ansible 預設讀取此目錄下的 ` main.yml `

##### 優先級 ( 高 到 低 )
1. ###### Extra vars：使用 "-e" 參數在命令行中定義的變量，具有最高優先級。
2. ###### Role vars：定義在角色中的變量，優先級高於 playbook 中定義的變量。
3. ###### Play vars：定義在 playbook 中的變量，優先級高於全局變量。
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
4. ###### Host vars：定義在 Inventory 中的變量，優先級高於全局變量。
5. ###### Group vars：定義在 Inventory 中的變量，優先級高於全局變量。
6. ###### Global vars：定義在 Ansible 配置文件中的全局變量，優先級最低。


###### [Ansible Doc to introduction var](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable)
