# pr police

## セットアップ

### 環境変数の設定

```
$ cp .env.example .env
```

`.env`、`slack_users.rb`の値を環境に合わせて変更してください。

### 起動

```
$ docker build -t pr_police
$ docker run pr_police
```

## デプロイ

### Heroku

```
$ git push heroku master
```

### Worker

```
$ heroku ps:scale worker=1 # 起動
$ heroku ps:scale worker=0 # 停止
```
