# Strapi application

A quick description of your strapi application


### Import db dump to docker container:

```sh
cat strapi.sql | docker exec -i api-strapi_postgres_1 psql -U strapi -d strapi -W strapi
```

### Dump db

```sh
docker exec -t api-strapi_postgres_1 pg_dump -c --if-exists --exclude-table=strapi_administrator -U strapi -d strapi -W strapi > dump_strapi_`date +%d-%m-%Y"_"%H_%M_%S`.sql
```