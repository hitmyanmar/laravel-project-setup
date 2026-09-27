
# Plain Laravel Project Setup

This guide shows how to create a **plain Laravel project** by cloning the official Laravel GitHub repository.

Official Repository:

https://github.com/laravel/laravel

---

# Before You Start

Make sure your development environment is ready.

You should have:

- PHP 8.3+
- Composer 2.x
- Node.js
- NPM
- Git
- MySQL, PostgreSQL, SQLite, or another supported database

---

# 1. Clone Laravel

Choose a directory where you want to create your project.

Then clone the official Laravel repository.

## SSH

```bash
git clone git@github.com:laravel/laravel.git my-project
```

## HTTPS

```bash
git clone https://github.com/laravel/laravel.git my-project
```

Replace:

```text
my-project
```

with your own project name.

Example:

```bash
git clone git@github.com:laravel/laravel.git blogging-system
```

---

# 2. Enter the Project

Move into the project directory.

```bash
cd my-project
```

Example:

```bash
cd blog
```

---

# 3. Remove Existing Git History

Because the project was cloned from Laravel's GitHub repository, it already contains Laravel's Git history.

For your own application, remove the existing `.git` directory.

## Git Bash

```bash
rm -rf .git
```

## Windows CMD

```cmd
rmdir /s /q .git
```

> This does not delete your Laravel project files. It only removes the existing Git repository information.

---

# 4. Install PHP Dependencies

Install Laravel's PHP dependencies using Composer.

```bash
composer install
```

---

# 5. Create the `.env` File

Laravel uses the `.env` file for application-specific configuration.

Copy:

```text
.env.example
```

to:

```text
.env
```

## Git Bash

```bash
cp .env.example .env
```

## Windows CMD

```cmd
copy .env.example .env
```

---

# 6. Generate Application Key

Generate the Laravel application key.

```bash
php artisan key:generate
```

Laravel will automatically update inside your `.env` file.

```env
APP_KEY=
```

---

# 7. Configure the Database

Laravel may use SQLite by default depending on the project version.

If you want to use **MySQL**, update your `.env` file.

Example:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=my_project
DB_USERNAME=root
DB_PASSWORD=
```

---

# 8. Run Database Migration

After configuring your database, run:

```bash
php artisan migrate
```

Laravel will create the default database tables.

---

# 9. Install Frontend Dependencies

Laravel includes frontend tooling powered by Vite.

Install the Node.js dependencies:

```bash
npm install
```

---

# 10. Run Frontend Development Server

Start Vite:

```bash
npm run dev
```

Keep this terminal running while developing your application.

---

# 11. Run Laravel

Open another terminal inside your project directory.

Run:

```bash
php artisan serve
```

Laravel will normally start at:

```text
http://127.0.0.1:8000
```

Open the URL in your browser.

---

# Development Setup

During development, you will normally have two terminals running.

## Terminal 1 — Laravel

```bash
php artisan serve
```

## Terminal 2 — Vite

```bash
npm run dev
```
