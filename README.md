# Laravel8-Docker-Template
Ready to go Laravel 8 starter template built into Docker image with MySQL included.

- Breeze auth scaffolding at http://localhost/login and so on.
- phpMyAdmin at http://localhost:8080/ 
- Composer 2 included.

This template was built and tested in WSL2 environment, while Chrome browser was running in Windows10 to visit the Laravel 8 application.

***For dev use only.***

## Setup instructions
1. Clone the repo
2. From within `application\` folder (which is the project root folder):
   - Run `$ php ../composer2/composer.phar install` to install vendor libraries
   - Run `$ chmod -R o+rw bootstrap/ storage/` to fix permission issues
   - Run `$ docker-compose up -d --build` to build and run the docker containers (this may take up to 10-15 mins)
   - Run `$ cp .env.example .env` to create an `.env` file
   - Run `$ docker-compose exec app /bin/bash` to enter the `app` docker container's CLI
3. Once within the `app` docker container's CLI as in `root@53fcfcee10d4:/srv/app#`, generate key using
   - `php artisan key:generate`
4. Visit http://localhost/ for Laravel app's homescreen and phpMyAdmin is at http://localhost:8080/
5. As the laravel app is now up and running, start modifying laravel code to suit your needs using an IDE like VS Code.

*Note to self: See Docker-Laravel-VueJS Summary.docx for instructions on building this template from scratch.*
