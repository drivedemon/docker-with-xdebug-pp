# Start setup environment landing-page-app

![myImage](https://media.giphy.com/media/xTiTnHvXHHxOTcdmxO/giphy.gif)

Main DB config for landing-page-app `base on docker config`
```
    - APP_URL={up ot you define in nginx config eg. http://dev-landing-page.peerpower.co.th}
    - PP_APP_URL={up ot you define in nginx config eg. http://dev-app.peerpower.co.th}
    - DB_HOST=landing-page-db
    - DB_DATABASE=pp-app-landing-page
    - DB_USERNAME=admin
    - DB_PASSWORD=1234
```
---
## Note
From example config I change service name in `docker-compose` file also you need to change some config in `env` and nginx conifg
