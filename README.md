# study-laravel
```
docker exec -it study-laravel_php-fpm bash
```
これでコンテナの中に入り、以下のコマンドでLaravelに必要なファイルをインストールする
```
composer install
npm install
```

localhost:8000で基本のページにアクセスできるようになる。

これを動かすための.envは現在公開していないので、以下のメールアドレスにご連絡を・・・

willow710kut@gmail.com

# laravelどこに配置？
webディレクトリ配下にあるstudy-laravelっていうプロジェクトで作ったらとりあえず動きます

# プロジェクト名を変えたい
nginx/conf.d/host.conf
```
    root /var/www/study-laravel/public;
```

docker-compose.yml
のstudy-laravelが出る場所全部

辺りを変えると幸せになります。
