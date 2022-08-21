![Constructor](./readme-sources/logo.svg)


## ➡️ Launching

1. At first install:

- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

2. Clone project:

```
git clone https://github.com/AlexGeniusMan/Agora-Hack-2022-RealityX project --recursive
cd project
```

3. Create .env file and add secrets to it:

```
# --- Proxy ---
# - Main
PROXY_PORT=8777

# --- Core Backend ---
# - Main
CORE_BACKEND_DEBUG_MODE=False
CORE_BACKEND_SECRET_KEY=YOUR_BACKEND_SECRET_KEY
CORE_BACKEND_ALLOWED_HOSTS=*
CORE_BACKEND_DEFAULT_DB=PostgreSQL
# - Default user
CORE_BACKEND_SUPERUSER_USERNAME=example@gmail.com
CORE_BACKEND_SUPERUSER_EMAIL=example@gmail.com
CORE_BACKEND_SUPERUSER_PASSWORD=Alpine12

# --- Database ---
# - Main
DB_HOST=db
DB_NAME=agora_db
DB_USER=agora
DB_PASSWORD=Alpine12
```

> - To generate new BACKEND_SECRET_KEY use [this](https://stackoverflow.com/a/57678930/14355198) instruction
> - BACKEND_ALLOWED_HOSTS must be a list of allowed hosts, separated by whitespaces. To see how to configure it, look at [this](https://docs.djangoproject.com/en/3.2/ref/settings/#allowed-hosts) instruction
> - For DB_HOST use 'db' - to use container db or 'YOUR_DB_HOST' - to use your db

4. Change frontend/.env file:

```
VUE_APP_BASE_URL=http://127.0.0.1:8777/
```

5. Launch with Docker Compose:

```
docker-compose up
```

> Done! Project launched.
