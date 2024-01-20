# Idempiere Docker 11  Production Deployment

## Install `docker` on your host system

```bash
curl -fsSL https://get.docker.com | sudo sh
```

## Add the current user to `docker` group 

This will help you to execute `docker` command without  `sudo`

```bash
sudo usermod -aG docker $USER
```

##  Update user's group access 

```bash
newgrp docker
```

`Note:` To update your group access persistently, log off and login back again.
 
## Install `docker-compose`

```bash
sudo apt install docker-compose
```

## Clone the repository to your docker host

```
git clone https://github.com/ceee-dev/docker-idempiere-11.git
```

##  Change the directory 
 
```
cd docker-idempiere-11
```
 
## Generate `.env` file

```bash
bash create-env.sh 
```

## Deploy iDempiere using `docker-compose`

```bash
docker-compose -f docker-stack.yml up -d
```
## Observing iDempiere docker logs 

```bash
docker-compose -f docker-stack.yml logs -f
```

## Removing iDempiere docker 

```bash
docker-compose -f docker-stack.yml down -v --rmi all --remove-orphans
```


