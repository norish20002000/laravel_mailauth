# docker_laravel_nginx_node

- laravel6.0用のコンテナのみ最小構成です。
- laravel6.0プロジェクト作成済。
- auth済。

## clone後手順
```bash
$ docker-compose up -d --build
$ docker-compose exec app composer install
$ docker-compose exec app cp .env.example .env
$ docker-compose exec app php artisan key:generate
$ docker-compose exec app php artisan migrate
$ docker-compose run node npm install
$ docker-compose run node npm run dev
```
