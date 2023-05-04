* ###### 根據 Ansible 運行時 tasks 狀態的改變來通知 (notify) handlers。
* ###### 無論有多少個 task notify 同一個 handler，該 handler 都只會運行一次。
* ###### 非常常見 handler 的實踐之一就是在檔案被修改後重啟 services。