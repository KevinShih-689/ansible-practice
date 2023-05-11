###### 這邊紀錄 Inventory 資訊，同時可以定義變數
* ### group_vars
    * ##### 針對 Group 的 Hosts 做變數管理
    * ##### 檔名一定要依照 Group 的名稱去命名
        * ###### hosts
        ```
        [DynasafeVM]
        RHCSAPrac ansible_user=root

        [DynasafeRockyLinux]
        RockyLinux ansible_user=root
        ```
        * ###### 檔名: ` ./group_vars/DynasafeVM.yml ` 、 ` ./group_vars/DynasafeRockyLinux.yml `
    * ##### 你可以在這邊定義sudo密碼，用於使用 `--become`變數時，不用再另外打密碼。 範例:
        ```
        ---
        ansible_become_password: XXXXXX
        ```
* ### host_vars
    * ##### 針對每一台機器做變數管理
    * ##### 檔名一定要依照機器的名稱去命名
        * ###### hosts
        ```
        [DynasafeVM]
        RHCSAPrac ansible_user=root

        [DynasafeRockyLinux]
        RockyLinux ansible_user=root
        ```
        * ###### 檔名: ` ./host_vars/RHCSAPrac.yml ` 、 ` ./host_vars/RockyLinux.yml `
    * ##### 你可以在這邊定義sudo密碼，用於使用 `--become`變數時，不用再另外打密碼。 範例:
        ```
        ---
        ansible_become_password: XXXXXX
        ```