zabbix-server60
=========

## これは何？

Zabbix Server 6.0 を導入する Playbook です。

- Zabbix database 作成
- Zabbix db user 作成
- Zabbix インストール

## Dependencies

- 01_common/common
- 02_web/httpd
- 03_app/php-fpm
- 04_database/mysql-server80

## 変数

```
zabbix_db_passwd: dwRW2unMunMF&T
```

License
-------

BSD

Author Information
------------------

- snkk1210