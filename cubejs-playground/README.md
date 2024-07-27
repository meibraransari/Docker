---
Created: 2024-07-27T21:10:04+05:30
Updated: 2024-07-27T21:16:06+05:30
Maintainer: Ibrar Ansari
---
# **CubeJS Playground Setup Guide for Linux**

### Required Tools for Environment Setup (Development)

1. Ubuntu OS
2. Latest Docker must be installed.
3. Docker Service must be up and running.

### Install docker if not installed
```
cd /tmp/ && curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
groupadd docker
sudo usermod -aG docker $USER
systemctl enable docker
Reboot required so, kindly reboot system to take effect.
```
### Create Required directories
```
mkdir -p ~/cube/model && chmod -R 755 ~/cube && cd ~/cube && pwd
```
### Create Database credentials file to map to cubejs playground
> nano .env 
```
CUBEJS_DB_TYPE=mssql
CUBEJS_DB_HOST=x.x.x.x
CUBEJS_DB_NAME=mydb1
CUBEJS_DB_USER=sa
CUBEJS_DB_PASS=your_secure_pass

CUBEJS_API_SECRET=972e63e0846268877042aaf0a662e673
CUBEJS_EXTERNAL_DEFAULT=true
CUBEJS_SCHEDULED_REFRESH_DEFAULT=true
CUBEJS_DEV_MODE=true
```

Note:- Set Database details as per your configuration
Other database type configuration guide available here: https://cube.dev/docs/product/configuration/data-sources

### Run docker container
```
docker pull cubejs/cube:latest
docker run -itd --name=cube --restart=always -p 4000:4000 --env-file=$(pwd)/.env  -v $(pwd)/.cubestore:/cube/data -v $(pwd):/cube/conf -v $(pwd)/model:/model -e CUBESTORE_REMOTE_DIR=/cube/data cubejs/cube:latest
docker logs -f cube
```
### Access using URL from browser.
http://<HOST_IP>:4000

### API Guide
```
REST API Endpoint: http://<HOST_IP>:4000/cubejs-api/v1/load
Websockets Endpoint: ws://<HOST_IP>:4000/
GraphQL Endpoint: http://<HOST_IP>:4000/cubejs-api/graphql
Ref: http://<HOST_IP>:4000/#/frontend-integrations
```

### Cubejs Playground Reference: 
https://github.com/cube-js/cube
https://hub.docker.com/r/cubejs/cube
https://cube.dev/docs/product/configuration/data-sources

### 💼 Connect with me 👇👇 😊

- 🔥 [**Youtube**](https://www.youtube.com/@DevOpsinAction?sub_confirmation=1)
- ✍ [**Blog**](https://ibraransari.blogspot.com/)
- 💼 [**LinkedIn**](https://www.linkedin.com/in/ansariibrar/)
- 👨‍💻 [**Github**](https://github.com/meibraransari?tab=repositories)
- 💬 [**Telegram**](https://t.me/DevOpsinActionTelegram)
- 🐳 [**Docker**](https://hub.docker.com/u/ibraransaridocker)