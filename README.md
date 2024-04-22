# Built With Laravel

<a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a>

<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>


## Requirements

* PHP 8.2
* Laravel 10
* MySQl || PgSQL
* Docker


### About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.



## Project Setup
This guide will help you set up and run your Laravel project using Docker containers.
### Installation

Step-by-step instructions on how to install and configure Sunbird project.

1. Clone this repository.
2. Navigate to the project directory: `cd project-directory`.
4. Configure environment variables (refer .env.example).

### Step 1: **Generate Project Skeleton**
To begin, run the following command to generate your project's skeleton:

`curl -s "https://laravel.build/project" | bash`
This command fetches Laravel's build script and initializes your project directory.

### Step 2: **Database Configuration**
Once inside your project directory, configure your .env file to specify your database settings and host address.

### Step 3: **Docker Container Setup**
Start the Docker containers for your application:

`./vendor/bin/sail up -d`
This command initializes the Docker containers needed for your Laravel application.

### Step 4: **Database Migrations**
Run your application's database migrations to set up the database schema:

Copy code
`./vendor/bin/sail artisan migrate`

### Step 5: Additional Configuration (Optional)
_If you need specific database services such as MySQL, Redis, or PostgreSQL, you can customize your Docker setup
accordingly_.

MySQL and Redis:
`curl -s "https://laravel.build/project?with=mysql,redis" | bash`

PostgreSQL:
`curl -s "https://laravel.build/project?with=pgsql" | bash`

### Step 6: **Docker Configuration**
Once your Docker containers are running, a docker-compose.yml file will be generated in your project directory. Ensure
that the service name in the docker-compose.yml file matches your project name.

### Step 7: **Run the Application**
_To start your Laravel application, use the following command:_


Replace project with your actual project name in the docker-compose command.
For example
`docker compose --profile project up`