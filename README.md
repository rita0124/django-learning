# django-site
A playground of Django

## Setup Environmant
### 安裝 Django
`pip install django`
透過 pip 來安裝 django
如果不知道什麼是 pip 那麼不建議您繼續看下去

### 測試安裝結果
`django-admin`
如果指令可以用的話代表有裝成功

### 起個專案
`django-admin startproject mysite`
創一個專案目錄，其中將會包含
* manage.py 這個檔案提供了許多小指令，用來管理 django 專案
* 與專案同名的模組目錄，此範例為 mysite 目錄

### 啟用 Django 伺服器
先切換目錄到含有 manage.py 的那一層
然後用下方指令...
`python manage.py runserver`
將會看到

```
Run 'python manage.py migrate' to apply them.
June 07, 2020 - 01:02:53
Django version 3.0.7, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.
```
表示伺服器正確啟用並且開放本機的 8000 port 作為網頁伺服器入口

### 初始化 資料庫
Django 主打 Model View Template
其中的 Model 泛指網站中的資料
最常見的情形就是把資料建模放到資料庫
並且從資料庫中提取資料

重點就是我們要用到資料庫
透過以下指令，將預設採用模組以及他們所需的資料表都建出來
`python manage.py migrate`

### 創立一個 django 超級使用者
Django 提供了 admin 模組，我們普通人可以透過下列方式
來使用別人做好的管理介面與機制
`python manage.py createsuperuser`
```
Username (leave blank to use 'user'): whoareyou
Email address: xxxxx@gmail.com
Password:
Password (again):
Superuser created successfully.
```

### 試試看 django 預設搭載的 admin 模組吧
自行在運作 django 時候 連 127.0.0.1/admin/
並且登入看看
你會發現一個很容易看懂的介面
它可以用來管理 model 們