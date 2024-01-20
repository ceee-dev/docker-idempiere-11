# Idempiere Docker 11  Production Deployment

## Install `docker` on your host system

```bash
curl -fsSL https://get.docker.com | sudo sh
```

## Install `docker-compose`

```bash
sudo apt install docker-compose
```

## Generate `.env` file

```bash
bash create-env.sh > .env
```

## Deploy iDempiere using `docker-compose`

```bash
docker-compose -f docker-stack.yml up -d
```
