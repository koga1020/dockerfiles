# Dockerfiles

## phoenix1.4
vim .env
```bash
APP_CODE_PATH_HOST=
PHOENIX_PORT=4000
WEBPACK_DEVSERVER_PORT=
```

### プロジェクトの作成
```bash
docker-compose run phoenix1.4 mix phx.new . --app hoge
```

### サーバー起動
```bash
docker-compose up -d phoenix1.4
```