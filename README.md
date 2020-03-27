# Laravel-Docker

Laravel-Docker is a basic setup for running Laravel applications locally with Docker.

## Installation

### Clone

- Clone this repo to your local machine.
- Clone the latest version of Laravel to a subdirectory which will contain your project:
```shell
$ git clone https://github.com/laravel/laravel.git YOUR_PROJECT_NAME
```

### Setup

- First run a `composer install` in the `YOUR_PROJECT_NAME`-folder:
```shell
$ docker run --rm --interactive --tty --user $(id -u):$(id -g) --volume $PWD:/app composer install
```
- Rename the `.env.example` file to `.env`:
```shell
$ mv .env.example .env
```
- Change the variables in the `.env`-file to work with your environment.
- Change the value of `LOCAL_WORKING_DIR` in the `.env`-file to point to the folder which contains your project.
- Create and run the containers:
```shell
$ docker-compose up -d
```
- Rename the `.env.example` file to `.env` in the `YOUR_PROJECT_NAME`-folder.
- Change `DB_CONNECTION` to `mysql` in the `.env` file.
- Change `DB_DATABASE`, `DB_USERNAME` and `DB_PASSWORD` so they match the settings in the `.env`-file in the root folder.
- Run in the root folder:
```shell
$ docker exec php php artisan key:generate
```