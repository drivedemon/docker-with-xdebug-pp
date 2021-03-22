# docker-with-xdebug-pp

![Alt Text](https://media.giphy.com/media/e5EcjjJx3dCFi/giphy.gif)

## Docker setup

Clone repo
```
git clone <Repository URL>
```

Copy to inside your project and change DB config
```
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=pp-app-main
MYSQL_USER=admin
MYSQL_PASSWORD=1234
```

Build Image
```
docker-compose up -d
```

## Done! setup docker
---

## Start setup project

Make new ENV
```
cp .env.example .env
```

Change DB config to
```
DB_HOST=db
DB_DATABASE=pp-app-main
DB_USERNAME=admin
DB_PASSWORD=1234
REDIS_HOST=redis
QUEUE_DRIVER=redis
FILESYSTEM_DRIVER=s3
```

Go to inside docker
```
docker exec -it <container_name> bash
```

Run require system setup
```
composer install
php artisan migrate
yarn install
yarn run dev
```

## Well done! Setup project finished~~
---

## Last step for mapping host in local machine

Shell to hosts file
```
sudo vi /etc/hosts
```

Add host name
```
127.0.0.1 dev-app.peerpower.co.th
127.0.0.1 dev-admin.peerpower.co.th
```
---

# Note
If you need adapt to other project just make sure your `(container name / mapping host / nginx config host)` correctly :)
