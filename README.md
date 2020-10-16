# Snipe-IT Docker Container

## Starting The Container (Not The First Time)

```
docker-compose up -d
```

## Staring The Container For The First Time

1. Generate ssl certificates with `./Config/gen_certs.sh`
2. Edit [env.local](./Docker/env.local)
3. Start the container with `docker-compose -f ./Docker/docker-compose.yml up -d`
4. Generate the app key with `docker exec -it snipe-it php artisan key:generate --force`
5. Stop running the docker container with `docker-compose -f ./Docker/docker-compose.yml down`
6. Replace `APP_KEY=<<Fill in Later!>>` in [env.local](./Docker/env.local) with the generated app key. It should look like `APP_KEY=base64:/uy+/djDi0n7ZHdlF/yx5AjM22xp2GBs7uHyc=`
7. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
