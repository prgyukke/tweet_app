# tweet_app
Qiitaの記事用のレポジトリです。

ビルトインサーバは自動起動です。  
`http://localhost:3000/`にて確認可能です。  
本レポジトリは[Docker_for_Ruby_on_Rails](https://github.com/prgyukke/Docker_for_Ruby_on_Rails)を基に作成しています。
アプリは[Progate](http://prog-8.com/)を基にしています。

## 環境構築
### 初回のみ
```
$ git clone git@github.com:prgyukke/tweet_app.git
$ cd tweet_app/
$ rm -rf .git
$ docker-compose up -d
```

appコンテナに入る
```
$ docker exec -it tweet_app_app_1 /bin/bash
# rails db:migrate
```

### 2回目以降
```
$ cd tweet_app/
$ docker-compose up -d
```

### コンテナに入る際
```
$ docker exec -it tweet_app_app_1 /bin/bash
```

### コンテナを抜ける際
```
# コンテナ上にて
# exit
```

### 開発終了時
```
$ docker-compose down
$ docker rmi tweet_app_app
```
