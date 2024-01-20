# Idempiere Docker 11  Production Deployment

## Generate `.env` file

```bash
bash create-env.sh > .env
```

## Deploy iDempiere using `docker-compose`

```bash
docker-compose -f docker-stack.yml up -d
```
