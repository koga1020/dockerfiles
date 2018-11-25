# Dockerfiles

## phoenix1.4
vim .env
```
APP_CODE_PATH_HOST=
PHOENIX_PORT=4000
WEBPACK_DEVSERVER_PORT=
```

### プロジェクトの作成
```
docker-compose run phoenix1.4 mix phx.new . --app hoge
```

### サーバー起動
docker-compose up -d phoenix1.4
