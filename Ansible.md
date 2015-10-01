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

