#Ansible


##基本的なこと

* ansible.cfg
* hosts
* playbook.yml

`ansible-playbook playbook.yml --private-key=xxx`


まずファイルの先頭の行にハイフン(-)を3つ書く。
これが、ここから YAML 文書の記述が始まる、という合図になる。

Ansibleの"-"は、同じ階層の要素を順番に並べて書くときに使う。
http://demand-side-science.jp/blog/2014/ansible-in-wonderland-03/


##SSHチューニング

[公式1](http://www.ansible.com/blog/ansible-performance-tuning)

[公式2](http://docs.ansible.com/ansible/intro_configuration.html#ssh-args)

[Qiita](http://qiita.com/kiida/items/3594a25b4e2e8695e2cb)


nsible-playbook -i hosts --private-key=~/.ssh/d1  playbook.yml



* ansible×weblogic

oracleからjdkをwgetする
```wget --no-check-certificate --no-cookies - --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/7u72-b14/jdk-7u72-linux-x64.rpm```


#エラー

```
msg: sudo: sorry, you must have a tty to run sudo
rsync: connection unexpectedly closed (0 bytes received so far) [sender]
rsync error: error in rsync protocol data stream (code 12) at io.c(605) [sender=3.0.9]
```

対象サーバのvisudoから設定変更

```
# visudo

Defaults requiretty
↓　↓　↓
#Defaults requiretty
or
Defaults !requiretty
```
