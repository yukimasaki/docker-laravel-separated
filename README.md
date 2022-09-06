# About
This repository is replicated using [ucan-lab/docker-laravel](https://github.com/ucan-lab/docker-laravel/) as a template.  
Source code and Docker files can be managed as independent repositories.

# Directory structures
```
docker-laravel
  ├── infra
  |    └─docker
  |        ├──app
  |        ├──web
  |        └──db
  └── src
```

# Applications
### app container
- Base image
  - [php](https://hub.docker.com/_/php):7.4.1-fpm
  - [composer](https://hub.docker.com/_/composer):2.4.1

### web container
- Base image
  - [nginx](https://hub.docker.com/_/nginx):1.22

### db container
- Base image
  - [mysql/mysql-server](https://hub.docker.com/r/mysql/mysql-server):8.0

### mailhog container
- Base image
  - [mailhog/mailhog](https://hub.docker.com/r/mailhog/mailhog)

# Usage
### A. Start with a new project.
1. Click [Use this template](https://github.com/yukimasaki/docker-laravel-separated/generate)
2. $ mkdir -p docker-laravel/infra
3. $ cd docker-laravel/infra
4. $ git clone `https://github.com/your-repository/replicated-template.git` .
5. $ make create-project # Install the latest Laravel project
6. $ make install-recommend-packages # Optional

### B. Start with an existing project.
1. Click [Use this template](https://github.com/yukimasaki/docker-laravel-separated/generate)
2. $ mkdir -p docker-laravel/infra
3. $ cd docker-laravel/infra
4. $ git clone `https://github.com/your-repository/replicated-template.git` .
5. $ git clone `https://github.com/existing/project.git` ../src
6. $ make init
