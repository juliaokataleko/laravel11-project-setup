# Laravel 11 project setup with InertiaJs using Vue

## Packages

Laravel Permission - https://spatie.be/docs/laravel-permission/v6/installation-laravel <br/>
Laravel Activity Log - https://spatie.be/docs/laravel-activitylog/v4/installation-and-setup<br/>
Laravel Media Library - https://spatie.be/docs/laravel-medialibrary/v11/installation-setup<br/>

## Installation

 - clone the repository: https://github.com/juliaokataleko/laravel11-project-setup
 - Create the .env file from .env.example
 ```
   cp .env.example .env
 ```
 - Install the compose dependencies
 ```
   docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php83-composer:latest \
    composer install --ignore-platform-reqs
```
- With docker started on your machine, start the project:
```
  ./vendor/bin/sail up -d
```
- Generate the application key
```
./vendor/bin/sail artisan key:generate
```
 - Run migration and data seeder
```
./vendor/bin/sail artisan migrate --seed
```

 - Install npm dependencies
```
./vendor/bin/sail npm i
```

 - Run npm
```
./vendor/bin/sail npm run dev
```

 - Access the platform
http://localhost
Admin credentials - login:admin@admin.com / password:admin