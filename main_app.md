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
```

Data mart config for main-app `require data mart app`
```
    - DATA_MART_ENABLED=true
    - DATA_MART_URL={up to you define host also base on docker extra host config}
    - DATA_MART_TOKEN={see in db data mart}

    - eg. DATA_MART_URL=http://dev-data-mart.peerpower.co.th:81
```

Landing page config for main-app `require landing page app`
```
    - LANDING_PAGE_ENABLED=true
    - LANDING_PAGE_URL={up to you define host also base on docker extra host config}
    - LANDING_PAGE_TOKEN={see in db landing page}

    - eg. DATA_MART_URL=http://dev-landing-page.peerpower.co.th:82
```

Credit score config for main-app `require credit score app`
```
    - CREDIT_SCORE_URL={up to you define host also base on docker extra host config}
    - CREDIT_SCORE_TOKEN={see in db credit score}

    - eg. DATA_MART_URL=http://dev-credit-score.peerpower.co.th:84
```

Sendinblue mail server config for main-app
> Ps: still error 100% coz template not exist if you need to see how it work please get `API_KEY` from prod
```
    - SENDINBLUE_ENABLED=false
    - SENDINBLUE_URL=https://api.sendinblue.com/v3/smtp/email
    - SENDINBLUE_API_KEY={register in www.sendinblue.com}
    - SENDINBLUE_TESTING_EMAIL={your email}
```
