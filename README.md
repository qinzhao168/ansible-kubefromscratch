---
layout: default
title:  README
author: lijiaocn
createdate: 2018/03/15 21:23:00
changedate: 2018/03/15 21:46:47

---

尚未完成，暂时保存，以防丢失...

创建python运行环境：

	virtualenv env

进入virtualenv创建的python运行环境：

	source env/bin/activate

第一次运行时，指定用户并输入密码，本地的公钥匙`~/.ssh/id_rsa.pub`会被添加到目标机器中，之后可以免密码登录。

	ansible-playbook -u vagrant -k -i inventories/staging/hosts all.yml

第二次，直接使用root用户，免密码：

	ansible all -u root -i inventories/staging/hosts -m command -a "pwd"
