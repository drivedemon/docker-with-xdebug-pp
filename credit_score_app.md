# Start setup environment credit-score-app

## so easy just clone docker and change service name then edit db config

![Alt Text](https://media.giphy.com/media/d3mlE7uhX8KFgEmY/giphy.gif)

Main DB config for credit-score-app `base on docker config`
```
    - DB_HOST=credit-score-db
    - DB_DATABASE=pp-app-credit-scroe
    - DB_USERNAME=admin
    - DB_PASSWORD=1234
```
---
## Note
From example config I change service name in `docker-compose` file also you need to change some config in `env` and nginx conifg
