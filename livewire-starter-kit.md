
# Laravel Livewire Starter Kit Setup

This guide shows how to create a **Laravel Livewire Starter Kit project** by cloning the official Laravel GitHub repository.

Official Repository:

[https://github.com/laravel/livewire-starter-kit](https://github.com/laravel/livewire-starter-kit)

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

# 1. Clone Laravel Livewire Starter Kit

Choose a directory where you want to create your project.

Then clone the official Laravel Livewire Starter Kit repository.

## Using SSH

```bash id="2jtg4e"
git clone git@github.com:laravel/livewire-starter-kit.git <project name>
```

## OR using HTTPS

```bash id="ql468e"
git clone https://github.com/laravel/livewire-starter-kit.git <project name>
```

---

# 2. Enter the Project

Move into the project directory.

```bash id="5ktqzg"
cd <project name>
```

---

# 3. Remove Existing Git History

Because the project was cloned from Laravel's GitHub repository, it already contains Laravel's Git history.

For your own application, remove the existing `.git` directory.

## Git Bash

```bash id="w8o3pf"
rm -rf .git
```

## Windows CMD

```cmd id="89bo6x"
rmdir /s /q .git
```

> This does not delete your Laravel project files. It only removes the existing Git repository information.

---

# 4. Install PHP Dependencies

Install Laravel's PHP dependencies using Composer.

```bash id="j8pbsi"
composer install
```

---

# 5. Create the `.env` File

Laravel uses the `.env` file for application-specific configuration.

Copy:

```text id="5h5wfm"
.env.example
```

to:

```text id="lhkg16"
.env
```

## Git Bash

```bash id="6yft3e"
cp .env.example .env
```

## Windows CMD

```cmd id="o47jwf"
copy .env.example .env
```

---

# 6. Generate Application Key

Generate the Laravel application key.

```bash id="ngodc1"
php artisan key:generate
```

Laravel will automatically update inside your `.env` file.

```env id="5frpsm"
APP_KEY=
```

---

# 7. Configure the Database

Laravel may use SQLite by default depending on the project version.

If you want to use **MySQL**, update your `.env` file.

Example:

```env id="i5v9c8"
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

```bash id="mhw2wq"
php artisan migrate
```

Laravel will create the default database tables.

---

# 9. Install Frontend Dependencies

The Laravel Livewire Starter Kit includes frontend tooling powered by Tailwind CSS and Vite.

Install the Node.js dependencies:

```bash id="0xifd2"
npm install
```

---

# 10. Run Frontend Development Server

Start Vite:

```bash id="f0hczv"
npm run dev
```

Keep this terminal running while developing your application.

---

# 11. Run Laravel

Open another terminal inside your project directory.

Run:

```bash id="bslhh3"
php artisan serve
```

Laravel will normally start at:

```text id="i84w6g"
http://127.0.0.1:8000
```

Open the URL in your browser.

---

# 12. Optional — Disable Email Verification

The Livewire Starter Kit may protect some pages using both:

```php id="udfcey"
'auth'
```

and:

```php id="v51l4h"
'verified'
```

For example:

```php id="z42i3y"
Route::middleware(['auth', 'verified'])->group(function () {
    Route::view('dashboard', 'dashboard')->name('dashboard');
});
```

If you do not want to use email verification yet, remove:

```php id="2t13je"
'verified'
```

Change:

```php id="1jkhhz"
Route::middleware(['auth', 'verified'])->group(function () {
    Route::view('dashboard', 'dashboard')->name('dashboard');
});
```

to:

```php id="wf1cxs"
Route::middleware(['auth'])->group(function () {
    Route::view('dashboard', 'dashboard')->name('dashboard');
});
```

> This is optional. Keep `verified` if you want users to verify their email address before accessing protected pages.

---

# 13. Authentication Already Included

The Livewire Starter Kit already includes authentication features such as:

- Register
- Login
- Logout
- Password reset
- Email verification
- Password confirmation
- Two-factor authentication
- Protected dashboard
- User profile/settings

So you do not need to build authentication from scratch before starting your project.

---

# 14. Important Livewire Starter Kit Files

Livewire projects are structured differently from the Vue, React, and Svelte starter kits.

Some important folders are:

```text id="0xq9po"
app/Livewire/
```

Livewire component classes.

```text id="1e7sr4"
resources/views/
```

Blade views.

```text id="p8bpxu"
resources/views/livewire/
```

Livewire component views.

```text id="n6zmsq"
resources/css/
```

Frontend styles.

```text id="u7bsm4"
resources/js/
```

Frontend JavaScript.

```text id="pl4ptj"
routes/web.php
```

Laravel web routes.

```text id="z7gdl0"
config/fortify.php
```

Authentication feature configuration.

```text id="q30kdr"
database/migrations/
```

Database migrations.

---

# 15. Livewire Starter Kit Stack

The Laravel Livewire Starter Kit uses:

```text id="vt2fcb"
Laravel
Livewire
Blade
Tailwind CSS
Vite
Laravel Fortify
```

Unlike the Vue, React, and Svelte starter kits, Livewire does not require Inertia for page rendering.

Most of your application can be built using:

```text id="m1cz4h"
PHP
Blade
Livewire
```

This makes Livewire a good choice if you prefer to stay mostly inside the Laravel and PHP ecosystem.

---

# Development Setup

During development, you will normally have two terminals running.

## Terminal 1 — Laravel

```bash id="71kzko"
php artisan serve
```

## Terminal 2 — Vite

```bash id="kp4otk"
npm run dev
```
