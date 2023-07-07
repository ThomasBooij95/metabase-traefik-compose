# About

A production ready docker compose file to deploy Metabase. Please refer to the official Metabase documentation for usage instructions.

## The compose file uses the following images:

- [Metabase](https://www.metabase.com/) – self-service BI reporting tool
- [Postgres](https://www.postgresql.org/) – database server used by the Metabase application
- [Traefik](https://traefik.io/) – a reverse proxy that sits in front of Metabase and provides SSL termination (and generates [Let's Encrypt](https://letsencrypt.org/) certificates)

⚠️ Docker images are continuously updated so please check the version tags and decide if you a newer version of the container would be more appropriate for your use case.

## Requires:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

# Configuration

Container configurations depend on environment variables defined in an .env file.

1. Duplicate the .env.example file and rename it to .env
2. Update the environment variables as needed
3. Update `db_password.txt`, `db_user.txt` and `mb_key.txt` following the instructions in each file.
4. Run `docker compose up -d` to create or update the docker containers from the compose file
4. Run `docker compose down` to shut down the containers

## Available environment variables

`MB_DBNAME`: name of the database

`MB_HOST`: the public URL that people will access Metabase from (assumes DNS is pointed correctly)

`LE_EMAIL`: for expiry notices when your certificate is coming up for renewal

# Contributing

Changes welcome! Please dont hesitate to open an issue if you spot a problem or make a pull request to propose an enhancement.