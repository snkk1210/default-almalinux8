roundcubemail
=========

## これは何？

Roundcube 導入 Playbook

## 変数

roundcubemail_password ← Roundcube ユーザ DB Password ( 適当な文字列 )  


```
---
  roundcubemail_password: sU9xaeg3#G5D
```


Dependencies
-------

- 02_web/httpd
- 03_app/php-fpm
- 04_database/mysql-server80
- 07_mail/roundcubemail

Other
-------
プロビジョニング後に下記に接続し設定を行う。  

http://[server ip]/roundcubemail/installer/

License
-------

BSD

Author Information
------------------

- keisuke sanuki 
