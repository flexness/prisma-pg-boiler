# stuff
- https://www.prisma.io/docs/getting-started/quickstart
- https://www.prisma.io/docs/orm/overview/databases/postgresql
- https://hub.docker.com/_/postgres

## steps
- init node project: `npm init -y`
- install req. npm ackages: `npm install typescript ts-node @types/node --save-dev`
- init typescript: `npx tsc --init`
- install prisma: `npm i prisma --save-dev`
- verify installlation: `run/init: npx prisma`
- initialize prisma for postgres: `npx prisma init --datasource-provider postgresql`
- `docker-compose up -d`
- `docker ps`
- access docker bash from container: `docker exec -it 923d51b9ec4b /bin/bash`
- run psql command on docker bash: `psql -U postgres -d mydb`
- add db schemas @ schema.prisma
- migrate db schema (create/update tables): `npx prisma migrate dev --name init`

## docker-postgres cmds
- `\q`: exit psql (postgres)
- `exit`: exit docker bash

![Alt text](migration.png)
![Alt text](dt-before-migrate.png)
![Alt text](dt-after-migrate.png)access-docker-postgres-bash.png
![Alt text](access-docker-postgres-bash.png)