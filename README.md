# レッスン1 DockerでWEBサーバを立ち上げて見よう

## 目的

このレポジトリでは、DockerをつかってWEBサーバを立ち上げて書いたHTMLが手元のパソコンのブラウザで表示できるところまでを目指しています。

## Dockerとは

細かい言葉や定義はあとでわかってくるので、まずはざっくりこんなもんかと思ってて大丈夫。はじめから「全部覚えるぞ!」ってやると挫折します。

1. Dockerはざっくり仮想環境です。
2. 仮想環境は手元で動いてるOSとは違うOSを立ち上げることができます。なので「仮想」
3. Windows上にLinuxを立ち上げることができます、Mac上でLinuxもできます。
4. チーム開発に向いてます。設定ファイルを渡すだけで、持ち運びがかんたんです、AさんのパソコンとBさんのパソコンで同じ環境をつくることができます。
5. リソースをそんなに消費しません。パソコンの動作が遅くなりにくいです。
6. 手元のパソコンを汚しません。不要になれば削除すれば終わりです。

というざっくりですが、こういう理由で昨今Dockerが人気です。むしろ開発現場ではDockerを使わずんば人にあらずぐらいな勢いになっています。

## DockerでWEBサーバを立ち上げてみよう

### 前準備

1. Microsoft社が無料で提供している、Visual Studio Codeをダウンロードしてインストールしましょう。Windows、Mac共に提供されています。Windowsの場合はダウンロードしたインストラーをダブルクリックして指示に従うだけでインストールできると思います。
   - https://code.visualstudio.com/
2. 同じようにDocker Desktopをダウンロードしてインストールしましょう。こちらも無料です。
   - https://docs.docker.com/desktop/
3. コンソールを使えるようにしよう
   - Windowsの場合は、Visual Studio Codeのアプリケーション内メニューにある「ターミナル」から新しいターミナルをクリックすれば画面下側に出現します。
   - Macの場合は、Terminal.appというアプリケーションが最初からインストールされていると思いますので、それを使ってください。
  
## Git cloneしてくる

```
hogehoge@localhost:$ git clone git@github.com:gachi-engineer/lesson1-docker.git
```

## 難しいことは何も考えずにDockerを立ち上げる

```
hogehoge@localhost:$ cd lesson1-docker/docker
hogehoge@localhost:$ docker compose up -d
[+] Running 8/8                                                                                                                                                                               
 ✔ myfirstapp-web Pulled                                                                                                                                                                 6.2s 
   ✔ a480a496ba95 Pull complete                                                                                                                                                          2.3s 
   ✔ f3ace1b8ce45 Pull complete                                                                                                                                                          3.0s 
   ✔ 11d6fdd0e8a7 Pull complete                                                                                                                                                          3.1s 
   ✔ f1091da6fd5c Pull complete                                                                                                                                                          3.1s 
   ✔ 40eea07b53d8 Pull complete                                                                                                                                                          3.1s 
   ✔ 6476794e50f4 Pull complete                                                                                                                                                          3.1s 
   ✔ 70850b3ec6b2 Pull complete                                                                                                                                                          3.1s 
[+] Running 2/2
 ✔ Network docker_default    Created                                                                                                                                                     0.1s 
 ✔ Container myfirstapp-web  Started 
```

## この画面が手元のパソコンのブラウザで表示されたらOK
http://localhost:8080/ にブラウザでアクセスしてみる。
<img src="https://raw.githubusercontent.com/gachi-engineer/lesson1-docker/refs/heads/develop/lesson/lesson1/screenshot.png" width="75%">
