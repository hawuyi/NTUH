# NTUH 台大黑名單專案
*主要流程  
 *擷取並建立/更新黑名單-> 黑名單更新至黑名單更新至防護安全設備（串接API）-> 定時清空黑名單

## 主要功能
* 用戶
 * 登入、登出、密碼重設
*擷取並建立/更新刪除搜尋黑名單至資料庫
    * 擷取黑名單:
      抓取網址（最後的數字從0開始0,1,2依序往下分頁，擷取至 Not found infomation / Internal Server Error/Internal Server Error 代表已結束）
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
*黑名單更新至黑名單更新至防護安全設備
    * 取得AED8100 collection網址:
      取得AED8100 collection網址，以做刪除黑名單資料、傳送資料至AED 8100使用
    * 黑名單更新至 AED 8100:
      存在資料庫黑名單資料傳送至AED 8100 (新增單項/多項黑名單)
    * collection網址更新與資料數量累計:
      資料傳送至AED 8100時，更新collection網址與資料數量累計至資料庫中
    * 黑名單更新至 AED 8100傳送資訊更新:
      傳送資訊資料更新至資料庫中
    * 黑名單更新至 AED 8100傳送資訊顯示前臺:
      查看傳送資訊詳細資料
    * 黑名單更新至 AED 8100傳送資訊刪除(單筆/多筆):
      刪除存在資料庫中的傳送資訊資料
    * 排程功能:
      定時刪除AED 8100 collection及資料庫黑名單資料
      定時擷取黑名單資料更新至資料庫及傳送至 AED 8100
    * 寄信功能:
      資料傳送至AED 8100 (新增單項/多項黑名單)錯誤時，啟動寄信功能
      刪除存在資料庫中的黑名單資料錯誤時，啟動寄信功能
      排程功能錯誤時，啟動寄信功能

## 運用技術
    1. PHP
    2. Laravel Framework 開發
    3. MySQL 管理資料庫
    4. Bootstrap  
    5. Node.js
***
### 專案截圖
