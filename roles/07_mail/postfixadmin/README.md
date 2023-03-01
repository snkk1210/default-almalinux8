postfixadmin（プレビュー）
=========

## これは何？

PostfixAdmin メールサーバ

- 自己証明書作成
- Postfix 設定調整
- Dovecot 導入/設定調整
- PostfixAdmin 導入/設定調整
- vmail ユーザ作成

## 変数

mail_domain ← PostfixAdmin ドメイン  
postfix_password ← PostfixAdmin ユーザ DB Password ( 適当な文字列 )  


```
---
  mail_domain: mail.develop.local
  postfix_password: sU9xaeg3#G5D
```


Dependencies
-------

- 02_web/httpd
- 03_app/php-fpm
- 04_database/mysql-server80

Other
-------
プロビジョニング後に下記に接続し設定を行う。  

http://[server ip]/postfixadmin/setup.php

License
-------

BSD

Author Information
------------------

- keisuke sanuki 
