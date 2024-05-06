# 黑名單專案
利用Laravel完成一個黑名單網站後台系統專案
* 主要流程  
  * 擷取並建立/更新黑名單-> 黑名單更新至防護安全設備（串接API）-> 定時清空黑名單

## 主要功能
* 用戶:
   * 登入、登出、密碼重設
* 擷取並建立/更新刪除搜尋黑名單至資料庫
  * 擷取黑名單:
     抓取網址內的IPv4和domain
  * 黑名單資料新增:
    將所有抓取到的黑名單全部新增至資料庫中
  * 黑名單資料更新:
    比對資料庫內容，將不存在資料庫中的資料更新至資料庫中
  * 黑名單資料顯示前臺:
    查看擷取黑名單明細資料
  * 黑名單資料刪除:
     刪除存在資料庫中的黑名單資料
  * 搜尋黑名單資料:
      搜尋黑名單 IP （包含 IP、加入/更新時間）
* 黑名單更新、刪除至防護安全設備
    * 取得防護安全設備 collection網址:
      取得防護安全設備 collection網址，以做刪除黑名單資料、傳送資料至防護安全設備使用
    * 黑名單更新至防護安全設備:
      存在資料庫黑名單資料傳送至防護安全設備 (新增單項/多項黑名單)
    * collection網址更新與資料數量累計:
      資料傳送至防護安全設備時，更新collection網址與資料數量累計至資料庫中
    * 黑名單更新至防護安全設備傳送資訊更新:
      傳送資訊資料更新至資料庫中
    * 黑名單更新至防護安全設備傳送資訊顯示前臺:
      查看傳送資訊詳細資料
    * 黑名單更新至防護安全設備傳送資訊刪除(單筆/多筆):
      刪除存在資料庫中的傳送資訊資料
    * 排程功能:
      定時刪除防護安全設備 collection及資料庫黑名單資料
      定時擷取黑名單資料更新至資料庫及傳送至防護安全設備
    * 寄信功能:
      資料傳送至防護安全設備(新增單項/多項黑名單)錯誤時、刪除存在資料庫中的黑名單資料錯誤時、排程功能錯誤時，啟動寄信功能
    * 功能錯誤時，記錄錯誤日誌
## 運用技術
    1. PHP 7.3
    2. Laravel Framework 5.8開發
    3. MySQL 管理資料庫
    4. Bootstrap
    5. SweetAlert2
***
### 專案截圖
![image](https://github.com/hawuyi/deny-list/assets/136839532/2776d240-fe7f-40dc-bb8a-d6c70c327c6c)

![image](https://github.com/hawuyi/NTUH/assets/136839532/4f0ac21d-d3b8-404c-8db9-b46fe4f3bb7d)

![image](https://github.com/hawuyi/NTUH/assets/136839532/9ce21f6c-45cc-4f04-9d2e-5ba69e116ad2)
![image](https://github.com/hawuyi/NTUH/assets/136839532/aed32edf-f013-4247-b988-eb99889da350)
![image](https://github.com/hawuyi/NTUH/assets/136839532/bc8d50dc-1fb6-4935-963c-ef6bc210161a)
![image](https://github.com/hawuyi/NTUH/assets/136839532/2f27f424-7c0a-4fc9-b699-9384c4171ae0)

![image](https://github.com/hawuyi/NTUH/assets/136839532/78175ac8-4ece-4e5f-9b5e-e3db8564acbe)









