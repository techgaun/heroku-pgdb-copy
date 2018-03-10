# heroku-pgdb-copy

> A plain simple bash script to copy and setup heroku database to your local postgres

### Usage

- Install [heroku-cli](https://devcenter.heroku.com/articles/heroku-cli)
- Make sure you are logged in: `heroku login`
- clone this repo or download the script from https://github.com/techgaun/heroku-pgdb-copy/raw/master/heroku-pgdb-copy

```shell
wget -O heroku-pgdb-copy https://github.com/techgaun/heroku-pgdb-copy/raw/master/heroku-pgdb-copy && chmod +x heroku-pgdb-copy
```

- Pass `HEROKU_APP` and `DATABASE_NAME` as the variables. These are the required variables.
- Optionally pass `DB_USER` and `PGPASSWORD` (defaults assumed by this script are `postgres` : `postgres`)
- If you have multiple pg database or non-standard database url, you can pass `HEROKU_DB_URL`

### Examples

```shell
$ HEROKU_APP=zego-stage DATABASE_NAME=zego-stage ./heroku-pgdb-copy

# custom database url
$ HEROKU_APP=zego-stage DATABASE_NAME=zego-stage HEROKU_DB_URL=HEROKU_POSTGRESQL_MAUVE_URL ./heroku-pgdb-copy

# custom pg user and password locally
$ HEROKU_APP=zego-stage DATABASE_NAME=zego-stage DB_USER=techgaun PGPASSWORD=hello123 ./heroku-pgdb-copy
```
