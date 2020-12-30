# hello-world

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

# How to deploy vuejs to cloudflare
## Create an account on cloudflare
https://dash.cloudflare.com/

1. Create a site: ex: localhost.com
2. Create a worker: go to site localhost.com created in step 1 > Workers > Manage Workers > Create a Worker

## Go to app Circleci
https://app.circleci.com/dashboard

1. Login by your Github account
2. Go to menu Projects >  Set Up Project > Use Existing Config > Star building
3. Step 2 should deploy fail. We must add variables for this project on Circleci
    
    3.1 Click on button Project Settings > Environment Variables > Add Environment Variable
    ```
    name: CLOUDFLARE_API_KEY
    value: Cloudflare API key (Go to cloudflare https://dash.cloudflare.com/profile/api-tokens > Use template of Edit Cloudflare Workers)

    name: CLOUDFLARE_ACCOUNT_ID
    value: Cloudflare account id
    ```

    3.2 Rebuild again