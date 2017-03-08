# sakura-vps-ubuntu-docker
さくらのVPSで、UbuntuにDockerをインストールする。

ついでに、`portainer`をインストール。

インベントリファイルを作成する。
(ファイル名を`inventory`としておく。)

```
[srv]
your.server

[srv:vars]
ansible_user=ubuntu
ansible_port=22
```

下記コマンド実行する。

```
$ ansible-playbook -kK -i inventory main.yml
```

