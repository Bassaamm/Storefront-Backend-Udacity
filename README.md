# Storefront Backend - Udacity Project

### Here is my solution for the project

## Set up the Environment variables first because docker set up depends on it

```sh
# for setting up the database
ENV=dev
POSTGRES_HOST=localhost
POSTGRES_PORT=5432
POSTGRES_DB=dev_db
POSTGRES_DB_TEST=test_db
POSTGRES_USER=root
POSTGRES_PASSWORD=root

# for the hashing and jwt
BCRYPT_PASSWORD=winteriscoming
TOKEN_SECERT=winteriscoming
SALT_ROUNDES=8
```

### the container need to be create first, run from the root of the project, make sure docker desktop is working

     $  docker-compose up

## Setting up the Database using psql

     $ docker exec -it storefrontbackend-udacityproject-postgres-1 bash

###

     $ psql postgres

###

```sh
    CREATE USER root WITH PASSWORD 'root';
    CREATE DATABASE dev_db;
    CREATE DATABASE test_db;
    GRANT ALL PRIVILEGES ON DATABASE dev_db TO root;
    GRANT ALL PRIVILEGES ON DATABASE test_db TO root;
```

## Setup to run the project

### Install dependencies

    $ npm i

## Run the migrations

    $ db-migrate up

### Run the project

    $ npm run start

### Build the project

    $ npm run build

### test the project

    $ npm run test

### Run jasmine

    $ npm run jasmine

### Run eslint

    $ npm run eslint

### Run Prettier

    $ npm run prettier
