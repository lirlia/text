
[Qiitaの参考記事](http://qiita.com/shouta-dev/items/8c9a6a2c360c0e2f71cd)

今回は/tmp/rpmsの下に配置した想定とします。

* Pages機能をonにすること

```
$ yum install -y createrepo
$ createrepo /tmp/rpms
```

```
$ git clone https://github.com/user/yumrepo.git
$ cd yumrepo
$ git checkout --orphan gh-pages
$ cp -R /tmp/rpms/* .
$ git commit -a -m "Add RPMs"
$ git push origin gh-pages
```

・/etc/yum.repos.d/myyum.repo
```
[repos.myrepo]
name=RedHat-$releasever - myyumrepo
baseurl=http://xx.xx.xx.xx/pages/username/repositry
enabled=1
gpgcheck=0
```

##テスト

`yum search xxx --disablerepo=\* --enablerepo="repos.myrepo"`


