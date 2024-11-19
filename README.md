# レッスン3 DockerでLaravelの初期画面を表示させる

## 目的

このレポジトリでは、DockerをつかってWEBサーバとphp-fpmを連携してPHPが実行できる環境でPHPのフレームワークLaravelを動かすところまで行います。

## Git cloneしてくる

```
hogehoge@localhost:$ git clone git@github.com.yuru.bo:gachi-engineer/lesson3-docker-laravel.git
```

## 難しいことは何も考えずにDockerを立ち上げる

```
hogehoge@localhost:$ cd lesson3-docker-laravel/docker
hogehoge@localhost:$ docker compose up -d
```

## composerで必要ライブラリをとってくる

```
hogehoge@localhost:$ docker exec -it myfisrtapp-app /bin/bash
root@abcdefg123:$ composer install
```

## Laravelのencryption keyをつくる

```
root@abcdefg123:$ php artisan key:generate

   INFO  Application key set successfully.  
```

## この画面が手元のパソコンのブラウザで表示されたらOK
http://localhost:8080/ にブラウザでアクセスしてみる。
<img src="https://raw.githubusercontent.com/gachi-engineer/lesson3-docker-laravel/refs/heads/master/lesson/lesson3/screenshot.png" width="75%">
