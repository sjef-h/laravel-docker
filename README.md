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

- Copy the `.env.example` file to `.env`:
```shell
$ cp .env.example .env
```
- Change the variables in the `.env`-file to work with your environment.
- Change the value of `LOCAL_WORKING_DIR` to point to the folder which contains your project.