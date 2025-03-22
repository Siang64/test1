# 簡易資料管理系統 

## 1. 專案介紹
本專案是一個基於 **PHP + MySQL** 的簡易資料管理系統，提供 **資料新增、編輯、刪除與顯示** 的基本功能，作為學習 PHP 與資料庫操作的範例。

## 2. 專案結構
```
test1/
├── 00.basic html.html    # 基本 HTML 範例
├── 00.basic php.php      # 基本 PHP 範例
├── 000.php               # 其他 PHP 測試檔案
├── 1.editUI.php         # 資料編輯介面
├── 1.insertUI.php       # 資料插入介面
├── 1.listUI.php         # 資料列表顯示介面
├── 2.delete.php         # 刪除資料的後端處理
├── 2.insert.php         # 新增資料的後端處理
├── 2.update.php         # 更新資料的後端處理
├── dbconfig.php         # 資料庫設定檔
├── guestbook.sql        # 資料庫結構 SQL 檔案
├── README.md            # 專案說明文件
```

## 3. 環境需求
- **XAMPP**（Windows/macOS）或 **LAMP**（Linux）
- **PHP 7.4 以上**
- **MySQL 5.7+ / MariaDB**

## 4. 安裝與設定
### 1️⃣ **將專案放入 `htdocs` 目錄**
- Windows: `C:\xampp\htdocs\test1`
- Linux/macOS: `/opt/lampp/htdocs/test1`

### 2️⃣ **建立 MySQL 資料庫**
1. 開啟瀏覽器，輸入 `http://localhost/phpmyadmin`
2. 建立 `test_db` 資料庫
3. 匯入 `guestbook.sql` 檔案

### 3️⃣ **修改 `dbconfig.php`**
確保資料庫連線資訊正確：
```php
$servername = "localhost";
$username = "root";
$password = ""; // 預設為空
$dbname = "test_db";
```

## 5. 使用方式
### 🔹 **啟動 Apache 和 MySQL**
- Windows: 開啟 `XAMPP Control Panel`，點擊 `Start` (Apache + MySQL)
- Linux/macOS: 在終端機執行：
  ```sh
  sudo /opt/lampp/lampp start
  ```

### 🔹 **開啟專案**
在瀏覽器輸入：
```
http://localhost/test1/1.listUI.php
```

## 6. 主要功能
| **功能**        | **檔案名稱**        | **說明** |
|----------------|-----------------|---------|
| **顯示資料**  | `1.listUI.php`  | 顯示所有資料 |
| **新增資料**  | `1.insertUI.php` + `2.insert.php` | 新增新資料 |
| **編輯資料**  | `1.editUI.php` + `2.update.php` | 修改現有資料 |
| **刪除資料**  | `2.delete.php`  | 刪除選定資料 |

## 7. 停止伺服器
- **XAMPP (Windows)**: 在 `XAMPP Control Panel` 點擊 `Stop`
- **Linux/macOS**: 
  ```sh
  sudo /opt/lampp/lampp stop
  ```


