# Laravel Job Board Application

This is a simple Laravel-based job board application that includes CRUD functionality, user authentication with policies, and the ability to send emails when a user creates a job post. The application also supports queues for handling background tasks.

## Features

-   Job creation, listing, updating, and deletion (CRUD)
-   User authentication and authorization using Laravel Policies
-   Email notifications on job creation
-   Queue handling for background tasks

## Installation Steps

Follow these steps to get the application up and running:

1. **Clone the repository**

    ```bash
    git clone <repository-url>
    cd <repository-folder>
    ```

2. **Install PHP dependencies using Composer**

    ```bash
    composer install
    ```

3. **Set up environment variables**

    ```bash
    cp .env.example .env
    ```

4. **Generate the application key**

    ```bash
    php artisan key:generate
    ```

5. **Configure the `.env` file**

    Update your `.env` file with your database and mail configuration settings.

6. **Run database migrations**

    ```bash
    php artisan migrate
    ```

7. **Seed the database**

    ```bash
    php artisan db:seed
    ```

8. **Serve the application locally**

    ```bash
    php artisan serve
    ```

9. **Install frontend dependencies**

    ```bash
    npm install
    npm run dev
    ```

10. **Run the Laravel Queue Worker**
    To handle background jobs such as email sending, run the queue worker:
    ```bash
    php artisan queue:work
    ```

## Password Setup for Users

1. **Generate a password hash**
   You can create a password hash using `tinker`:

    ```bash
    php artisan tinker
    echo Hash::make('your_password');
    ```

2. **Update User Password in the Database**

    Use the generated password hash to update the password of a specific user in your database. You can do this via a database management tool like phpMyAdmin.

3. **Log in and test the application**
