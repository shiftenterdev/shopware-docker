# Shopware Docker **Experimental
### Based on `https://github.com/markshust/docker-magento`

__Installation:__

```shell
git clone https://github.com/shiftenterdev/shopware-docker.git

cd shopware-docker

# Install Shopware application
composer create-project shopware/production:6.5.8.9 src --ignore-platform-reqs

# Or clone your existing Shopware application
git clone https://github.com/shopware/production.git src
bin/composer install

# Start Docker
bin/start

# Stop Docker
bin/stop

# Restart Docker
bin/restart

````

__Available Command:__

| Command             | Task                                             |
|---------------------|--------------------------------------------------|
| `bin/start`         | Start containers                                 |
| `bin/stop`          | Stop containers                                  |
| `bin/console`       | Run shopware `bin/console` commands              |
| `bin/download`      | Download shopware repository                     |
| `bin/restart`       | Restart all containers                           |
| `bin/rebuild`       | Rebuild and recreate the containers              |
| `bin/removeall`     | Remove all containers and volumes                |
| `bin/bash`          | Go to container bash                             |
| `bin/npm`           | Run npm command                                  |
| `bin/node`          | Run node command                                 |
| `bin/docker-stats`  | Docker container statistics                      |
| `bin/composer`      | Run composer command                             |
| `bin/xdebug`        | Run xdebug command                               |
| `bin/setup-domain`  | Add domain for local development in `/etc/hosts` |
| `bin/remove-domain` | Remove domain                                    |


__Create Certificate:__
```shell
mkdir -p certs
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout certs/your-domain.com.key -out certs/your-domain.com.crt
```
