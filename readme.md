# Zabbix Deployment

## Deploy production environment

- Create AWS Postgres RDS instance
- Create AWS docker node instance
- Clone this repo on docker node: `git clone git@github.com:SindriaInc/zabbix-deployment.git`
- Change directory: `cd zabbix-deployment`
- Clean up local repo: `rm -Rf .git` 
- Customize values: `env_vars/.env_web` AND `env_vars/.env_db_pgsql`
- Inject secrets: `env_vars/.POSTGRES_USER` AND `env_vars/.POSTGRES_PASSWORD`
- Setup compose: `cp docker-compose.production.yml docker-compose.yml`
- Apply deployment: `docker-compose up -d`

## Deploy local environment

- Clone this repo on docker node: `git clone git@github.com:SindriaInc/zabbix-deployment.git`
- Change directory: `cd zabbix-deployment`
- Clean up local repo: `rm -Rf .git`
- Setup compose: `cp docker-compose.local.yml docker-compose.yml`
- Apply deployment: `docker-compose up -d`