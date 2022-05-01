php
=========

## これは何？

PHP と PHP モジュールをインストールする playbook です。

- レポジトリの追加
- PHP インストール
- 各種モジュールインストール
- php.ini 設定

## 変数

php_var に導入する php のバージョンを定義して下さい。  
php_modules に導入するモジュールを定義して下さい。

```
---
  php_var: 8.1
  php_modules:
    - "php"
    - "php-pdo"
    - "php-mbstring"
    - "php-gd"
#    - "php-curl"
#    - "php-pear"
#    - "php-bcmath"
#    - "php-gmp"
#    - "php-intl"
    - "php-mysqlnd"
```

License
-------

BSD

Author Information
------------------

- keisuke sanuki 