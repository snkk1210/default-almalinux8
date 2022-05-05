nginx
=========

## これは何？

nginx の基本的な設定を行う playbook です。  

- nginx インストール
- ドキュメントルート作成
- バーチャルホスト設定
- php-fpm の upstream 追加

## 変数

domain_name に設定するドメインと OS ユーザを指定して下さい。  
custom_domain はドキュメントルートを指定することができます。  
※ いずれも必須ではないです。

```
---
   domain_name:
      - { domain: 'test1.com' ,customer: 'testuser1' }
      - { domain: 'test2.com' ,customer: 'testuser2' }
   custom_domain:
      - { domain: 'ease.fingerease.work' ,customer: 'vagrant' , document_root: '/home/vagrant/public_html' }
```

License
-------

BSD

Author Information
------------------

- keisuke sanuki 
