# docker-compose-sentry

A simple setup for running [Sentry](https://getsentry.com/).

## Initial setup

In order to run Sentry, the database has to be initialized first:

1. Edit `docker-compose.yml` and set `POSTGRES_PASSWORD` and `SENTRY_SECRET_KEY`
1. Start Redis and Postgres: `docker-compose up -d redis postgres`
1. Load initial data: `docker-compose run --rm sentry upgrade`
1. Then start Sentry: `docker-compose up -d`
