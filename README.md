# Java8 + ApacheSolr4.5.1 (日本環境）

オフィシャルのjava8を元に日本環境の調整を行いました。

### 調整内容 ###

* locale設定 (ja.utf-8)
* タイムゾーン （Asia/Tokyo）
* 必要なツールのインストール  
※ less lsof procps wget curl vim
* Apache Solr 4.5.1

### 使い方 ###

下記のコマンドにてコンテナを起動します

```
$ docker pull reflet/docker-solr4
$ docker run -d --name embulk reflet/docker-solr4
$ docker exec -it solr4 bash
```

### メンテナンス ###

下記のコマンドにてソースのダウンロードとイメージの構築を実行します。

```
$ git clone git@github.com:reflet/docker-solr4.git .
$ docker build -t reflet/docker-solr4 .
$ docker login
$ docker tag reflet/docker-solr4 reflet/docker-solr4:{タグ}
$ docker push reflet/docker-solr4
```
