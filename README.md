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

Change DB config

>[Main-app-config](https://github.com/drivedemon/docker-with-xdebug-pp/blob/master/main_app.md)

>[Loan-beta-config](https://github.com/drivedemon/docker-with-xdebug-pp/blob/master/loan_beta_app.md)

>[Data-mart-config](https://github.com/drivedemon/docker-with-xdebug-pp/blob/master/data_mart_app.md)

Go to inside docker
```
docker exec -it <container_name> bash
```

Run install dependencies
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
> If you need adapt to other project just make sure your `(container name / docker db config / env db config / mapping host / nginx config host)` correctly :)
