default-almalinux8
=========

## これは何？

- AlmaLinux8 の Ansible playbook です。

## ディレクトリ構成

### group_vars/all.yml
変数を定義するファイルです。

### hosts
inventorys ファイルです。

### target.yml
main の playbook です。

### key
OS ユーザの秘密鍵を設置します。

### roles
各種 playbook を纏めています。

## 使い方

### 1.リポジトリを clone

```
git clone https://github.com/keisukesanuki/default-almalinux8.git
cd default-almalinux8
```

### 2.要件に併せて roles 以下の playbook をインクルード

```
vi target.yml
```

※ 下記のように必要な playbook をインクルードして下さい。

```
  roles:
    - 00_dummy
    - 01_common/common
    - 01_common/swap
    - 01_common/useradd_with_key
    - 01_common/tools
    - 02_web/httpd
    #- 02_web/nginx
    #- 03_app/php
    - 03_app/php-fpm
    #- 04_database/mysql-client80
    - 04_database/mysql-server80
    - 05_logs/httpd
    #- 05_logs/nginx
    - 05_logs/mysql
    - 05_logs/syslog
    - 06_monitor/zabbix-agent50
    #- 06_monitor/zabbix-proxy50
    - 06_monitor/zabbix-mysql-agent
```

### 要件に併せて変数を定義

```
vi group_vars/all.yml
```

どのような変数を定義する必要があるかについては、各種 role の README を参照して下さい。

### inventory ファイルを編集

```
vi hosts
```

左側にホスト/右側にIPアドレスを指定して下さい。  
※ 複数指定可能です。

```
[target]
target-node01 ansible_host=xxx.xxx.xxx.xxx
```

### 実行


・パスワード指定

```
ansible-playbook -i hosts target.yml --ask-pass
```

・秘密鍵指定

```
ansible-playbook -i hosts target.yml --private-key=privatekey.pem
```

### 実行(ドライラン)

```
ansible-playbook -i hosts target.yml --ask-pass -C
```

・秘密鍵指定

```
ansible-playbook -i hosts target.yml --private-key=privatekey.pem -C
```

License
-------

BSD

Author Information
------------------

- keisuke sanuki 