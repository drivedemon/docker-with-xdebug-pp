# Start setup environment main-app

![myImage](https://media.giphy.com/media/XRB1uf2F9bGOA/giphy.gif)

Main DB config for main-app `base on docker config`
```
    - APP_URL={up ot you define in nginx config eg. http://dev-app.peerpower.co.th}
    - ADMIN_URL={up ot you define in nginx config eg. http://dev-admin.peerpower.co.th}
    - DB_HOST=db
    - DB_DATABASE=pp-app-main
    - DB_USERNAME=admin
    - DB_PASSWORD=1234
    - REDIS_HOST=redis
    - QUEUE_DRIVER=redis
    - FILESYSTEM_DRIVER=s3
    - AWS_KEY={please ask team lead}
    - AWS_SECRET={please ask team lead}
    - S3_BUCKET=peerpower-dev
    - S3_ASSET_BUCKET=peerpower-assets
    - DEFAULT_QUEUE=pp_default
```

Data mart config for main-app `require data mart app`
```
    - DATA_MART_ENABLED=true
    - DATA_MART_URL={up to you define host also base on docker extra host config}
    - DATA_MART_TOKEN={see in db data mart}

    - eg. DATA_MART_URL=http://dev-data-mart.peerpower.co.th:81
```

Sendinblue mail server config for main-app
> Ps: still error 100% coz template not exist if you need to see how it work please get `API_KEY` from prod
```
    - SENDINBLUE_ENABLED=false
    - SENDINBLUE_URL=https://api.sendinblue.com/v3/smtp/email
    - SENDINBLUE_API_KEY={register in www.sendinblue.com}
    - SENDINBLUE_TESTING_EMAIL={your email}
```
