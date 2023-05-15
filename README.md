# README

## FerretDB + postgresql のお試し環境 with Go

### `env`の準備

`ferretdb`ディレクトリで以下を実行

```sh
cp .env.sample .env
```

環境変数`POSTGRES_PASSWORD`は任意に設定してよい
(`POSTGRES_USER`まで変えるとデフォルトDBと合わなくなるのでもうひと工夫必要)

### docker compose

コンテナ外で`ferretdb`下で`docker compose up -d`してferretdb、postgresqlを起動する

> postgresql本体にも接続してみるので、5432をexposeする
> ホストのディレクトリへのマウントが推奨されないとのことで、persistentはvolumeにする
> VSCodeのpostgresとmongodb拡張で両方とも接続できたことを確認

## 記事

[MongoDB の初体験環境を FerretDB で構築してみた](https://zenn.dev/daifukuninja/articles/9dfc2d7d877aef)
