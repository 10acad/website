# 10academy Web

The 10academy wordpress website.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development. 
See deployment for notes on how to get website live.

### Prerequisites

* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Make](https://www.gnu.org/software/make)
* [Docker + Docker Compose](https://docs.docker.com/docker-for-mac/install/) 

### Installing

```sh
git clone git@bitbucket.org:10academy/website.git ## Clone repo
cd website
make init ## Builds and sets up containers
```

And wait for it to end.


Now you can view:
* website at [localhost:8000](http://localhost:8000/)
* phpomyadmin at [localhost:3333](http://localhost:3333/)

### Commands
```sh
make init ## Initialize docker container and run on initial setup
make rebuild ## Rebuilds containers
make rebuildprod ## Rebuilds containers on live
make restartprod ## Restarts containers on live
```

### Production
* SSL is generated with certbot docker container and automatically renewed
* Redis is actually used for pagespeed to boost speed of delivery
* Nginx pagespeed uses ./conf/pagespeed.conf for its settings
* Mysql on live is externalized into an RDS

## Deployment

```sh
make deploy
```
