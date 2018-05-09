# CentOS, Apache, PHP7 with Docker Compose

![](http://sheershoff.ru/wp-content/uploads/2018/01/docker-php-640x276.png)

※ MacでDocker composeを使ったPHP開発環境  
  
## Dockerのインストール
- Docker for Macを落とす  
[https://docs.docker.com/docker-for-mac/install/](https://docs.docker.com/docker-for-mac/install/)
  

## How to start 

```
git clone https://github.com/hiroki-tkg/php-apache-env.git
mv php-apache-env [任意の開発用ディレクトリ名] 
cd [任意の開発用ディレクトリ名]

# 環境git関連削除
rm -rf .git
rm -f .gitignore

# Docker Compose をデタッチで起動
docker-compose up -d 

```
※ Docker for Macをインストールすると、Docker Composeもセットでついてきます。

dockerがちゃんと動けば、以下ですぐにPHP7.2系/Apache環境にアクセスできます。  
[http://localhost:7000](http://localhost:7000)

一瞬でできるし、環境がコードベースなので、差異がありません。すごい。

作成 : `<tkg.japan@gmail.com>`  



Document Rootは  `src ` 以下なので、そこを編集する。

### 起動済みDockerコンテナにbashで入る
```
docker exec -i -t [CONTAINER_ID] /bin/bash
```