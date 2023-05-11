# Development scripts
Some usefull scripts for development

## Examples

### db-docker
db-docker is a script to create database services in docker compose quickly and easily.

```bash
db-docker --list

#SQL databases:
#postgres       image: postgres:14.5
#mysql          image: mysql:8.0.33
#mariadb        image: mariadb:10.11.2
#
#Cache databases:
#redis          image: redis:7.0.7-alpine
#memcached      image: bitnami/memcached:latest

db-docker -s postrges -c redis

#[+] Running 3/3
# ✔ Network tmp_db_docker_net  Created
# ✔ Container postgres_docker  Started
# ✔ Container redis_docker     Started

db-docker --down

#[+] Running 3/3
# ✔ Container postgres_docker  Removed
# ✔ Container redis_docker     Removed
# ✔ Network tmp_db_docker_net  Removed
```


## Install

```bash
git clone https://github.com/Mth-Ryan/development-scripts $HOME/.development
# if you use bash:
echo "export PATH=$PATH:$HOME/.development/bin" >> .basrc
# if you use zsh:
echo "export PATH=$PATH:$HOME/.development/bin" >> .zshrc
./symlinks.sh
```
