# Shopware Docker **Experimental
Based on `https://github.com/markshust/docker-magento`

### Installation:

__Clone Repository:__
```shell
git clone https://github.com/shiftenterdev/shopware-docker.git

cd shopware-docker
````

__Create Certificate:__
```shell
bin/ssl-certificate
```

__Add shopware application(new/existing):__

```shell
# Install Shopware application
composer create-project shopware/production:6.5.8.9 src --ignore-platform-reqs

# Or clone your existing Shopware application
git clone https://github.com/shopware/production.git src
bin/composer install
```

__Start Docker:__
```shell
# Start Docker
bin/start

````

__Add domain:__
```shell
bin/setup-domain shopware101.local
```

Go to browser and open `https://shopware101.local`

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
| `bin/mysql`         | Run mysql command                                |
| `bin/mysqldump`     | Mysqldump command                                |
| `bin/npm`           | Run npm command                                  |
| `bin/node`          | Run node command                                 |
| `bin/docker-stats`  | Docker container statistics                      |
| `bin/composer`      | Run composer command                             |
| `bin/xdebug`        | Run xdebug command                               |
| `bin/setup-domain`  | Add domain for local development in `/etc/hosts` |
| `bin/remove-domain` | Remove domain                                    |

