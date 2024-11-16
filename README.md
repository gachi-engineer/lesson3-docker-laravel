# レッスン2 DockerでWEBサーバとphp-fpmを連携する

## 目的

このレポジトリでは、DockerをつかってWEBサーバとphp-fpmを連携してPHPが実行できる環境を構築することを目指します。

## Git cloneしてくる

```
hogehoge@localhost:$ git clone git@github.com.yuru.bo:gachi-engineer/lesson2-docker-php-fpm.git
```

## 難しいことは何も考えずにDockerを立ち上げる

```
hogehoge@localhost:$ cd lesson2-docker-php-fpm/docker
hogehoge@localhost:$ docker compose up -d

```

## この画面が手元のパソコンのブラウザで表示されたらOK
http://localhost:8080/ にブラウザでアクセスしてみる。
<img src="https://raw.githubusercontent.com/gachi-engineer/lesson2-docker-php-fpm/refs/heads/master/lesson/lesson2/screenshot.png" width="75%">
