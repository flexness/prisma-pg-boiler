# stuff
- https://www.prisma.io/docs/getting-started/quickstart
- https://www.prisma.io/docs/orm/overview/databases/postgresql
- https://hub.docker.com/_/postgres

## steps
- init node project: `npm init -y`
- install req. npm ackages: `npm install typescript ts-node @types/node --save-dev`
- init typescript: `npx tsc --init`
- install prisma: `npm i prisma --save-dev`
- verify installlation: `npx prisma`
- initialize prisma for postgres: `npx prisma init --datasource-provider postgresql`
- run docker compose `docker-compose up` (based on docker-compose.yml; `-d`: detached from terminal)
- show running containers:`docker ps -a` (`-a`for all)
- test tcp: `test-NetConnection -ComputerName localhost -Port 5432`
- access docker bash from container: `docker exec -it <containerid> /bin/bash`
- run psql command on docker bash: `psql -U postgres -d <dbname>`
- terminal access on postgres <dbname>, show tables: `\dt`
- add basic db schemas ~tables @ `schema.prisma`
- migrate db schema (create/update db tables): `npx prisma migrate dev --name init`
- migrate adds `"@prisma/client": "^5.10.2"`as dependency

## docker cmds
(docker-compose.yml is used as default)
- start docker container: `docker-compose up`
- stop docker container: `docker-compose stop` 
- remove docker environment: `docker-compose down`
- remove docker environment, including data (volumes): `docker-compose down -v`

## docker-postgres cmds
- psql: `\dt`
- psql: `\q`
- docker bash: `exit`

## screens
docker compose and docker ps:

![Alt text](docker-compose-docker-ps.png)

check if tcp connection is available:

![Alt text](test-tcp-netconnection.png)

access docker and postgres after init:

![Alt text](access-docker-postgres-bash.png)

show tables of initialized db:

![Alt text](dt-before-migrate.png)

migrate the added database schema (tables)

![Alt text](migration.png)

show tables after migration:

![Alt text](dt-after-migrate.png)


## low iq diagram
[<img src="image.png" width="250"/>](low-iq-diagram.excalidraw.png)