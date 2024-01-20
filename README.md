# Idempiere Docker 11  Production Deployment

## Install `docker` on your host system

```bash
curl -fsSL https://get.docker.com | sudo sh
```

## Add the current user to `docker` group 

This will help you to execute `docker` command without  `sudo`

```bash
sudo usermod -aG docker 



## Install `docker-compose`

```bash
sudo apt install docker-compose
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


