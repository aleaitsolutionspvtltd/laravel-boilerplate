Project Setup Guide
This guide will help you set up and run your Laravel project using Docker containers.

Step 1: **Generate Project Skeleton**
To begin, run the following command to generate your project's skeleton:

`curl -s "https://laravel.build/project" | bash`
This command fetches Laravel's build script and initializes your project directory.

Step 2: **Database Configuration**
Once inside your project directory, configure your .env file to specify your database settings and host address.

Step 3: **Docker Container Setup**
Start the Docker containers for your application:

`./vendor/bin/sail up -d`
This command initializes the Docker containers needed for your Laravel application.

Step 4: **Database Migrations**
Run your application's database migrations to set up the database schema:

Copy code
`./vendor/bin/sail artisan migrate`

Step 5: Additional Configuration (Optional)
If you need specific database services such as MySQL, Redis, or PostgreSQL, you can customize your Docker setup
accordingly.

MySQL and Redis:
`curl -s "https://laravel.build/project?with=mysql,redis" | bash`

PostgreSQL:
`curl -s "https://laravel.build/project?with=pgsql" | bash`

Step 6: **Docker Configuration**
Once your Docker containers are running, a docker-compose.yml file will be generated in your project directory. Ensure
that the service name in the docker-compose.yml file matches your project name.

Step 7: **Run the Application**
To start your Laravel application, use the following command:

bash
Copy code
docker-compose up -d
Replace project with your actual project name in the docker-compose command.