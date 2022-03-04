# Ruby on Rails

## Rails on Docker

### 参考 Docs

- https://github.com/kkoji/rails-lecture/tree/new_rails_pj
- https://github.com/kkoji/rails-lecture/tree/docker-files

docker-compose.yml ファイルの置いてあるディレクトリで実行する

Rails のコンテナを起動して Rails のプロジェクトを作成するコマンド

`$ docker-compose run web rails new . --force --database=mysql`

Rails イメージのビルド実行コマンド

`$ docker-compose build`

- config/database.yml の修正内容
- default 内の項目を修正
  password: password
  host: db

コンテナをデタッチドモード（バックグラウンド）で実行するコマンド

`$ docker-compose up -d`

Rails のコンテナで DB 作成のタスクを実行するコマンド

`$ docker-compose run web bundle exec rake db:create`
