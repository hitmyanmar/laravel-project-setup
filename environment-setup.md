
# Laravel Development Environment Setup

Before creating or running a Laravel project, make sure your computer has the required development tools installed.

This environment setup is shared by all of the guides in this repository:

- Plain Laravel
- Laravel Vue Starter Kit
- Laravel React Starter Kit
- Laravel Svelte Starter Kit
- Laravel Livewire Starter Kit

---

# 1. Requirements

For Laravel 13 development, make sure you have the following tools installed.

## Required

- PHP 8.3 or higher
- Composer 2.x
- Node.js
- NPM
- Git
- A database such as:
  - MySQL
  - PostgreSQL
  - SQLite
  - MariaDB

Laravel 13 requires a minimum of:

```text
PHP 8.3+
```

For a new setup, a modern Node.js LTS version is recommended.

Recommended:

```text
PHP:      8.3+
Composer: 2.x
Node.js:  24 LTS
NPM:      Included with Node.js
Git:      Latest stable version
```

> Node.js requirements can change depending on the frontend tooling and packages used by a starter kit. Using the current LTS version is usually the safest choice for a new development environment.

---

# 2. Check Your Environment

Open your terminal and run the following commands.

---

## Check PHP

```bash
php -v
```

Example:

```text
PHP 8.4.x
```

Your PHP version should be:

```text
8.3 or higher
```

---

## Check Composer

```bash
composer -V
```

Example:

```text
Composer version 2.x
```

If Composer is not recognized, Composer may not be installed or may not be added to your system PATH.

---

## Check Node.js

```bash
node -v
```

Example:

```text
v24.x.x
```

For new Laravel projects, Node.js 24 LTS is recommended.

---

## Check NPM

```bash
npm -v
```

Example:

```text
11.x.x
```

NPM is normally installed together with Node.js.

---

## Check Git

```bash
git --version
```

Example:

```text
git version 2.x.x
```

---

# 3. Quick Environment Check

You can check everything at once:

```bash
php -v
composer -V
node -v
npm -v
git --version
```

If all commands return version information without errors, your basic Laravel development environment is ready.

---

# 4. PHP Extensions

Laravel also requires several PHP extensions.

Common required extensions include:

```text
BCMath
Ctype
cURL
DOM
Fileinfo
Filter
Hash
Mbstring
OpenSSL
PCRE
PDO
Session
Tokenizer
XML
```

Most modern PHP development environments already include these extensions.

If Laravel or Composer reports that an extension is missing, check your `php.ini` file and enable the required extension.

---

# 5. Database

Laravel supports several database systems.

For beginners, MySQL is a common choice.

Example local MySQL configuration:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=my_project
DB_USERNAME=root
DB_PASSWORD=
```

Before running migrations, make sure the database exists.

Example database name:

```text
my_project
```

You can create your database using tools such as:

- phpMyAdmin
- HeidiSQL
- MySQL Workbench
- Laragon
- MySQL command line

Laravel can also use SQLite if you prefer a simpler local setup.

---

# 6. Windows Recommendation

For Windows beginners, using a local development environment can make PHP and database setup easier.

Common options include:

- Laragon
- Laravel Herd
- XAMPP

For Laravel development, Laragon or Laravel Herd are usually easier to work with than manually configuring PHP, MySQL and web server settings.

---

# 7. Check Which PHP Is Being Used

Sometimes multiple PHP versions are installed on the same computer.

Run:

```bash
php -v
```

Then check the PHP location.

## Windows CMD

```cmd
where php
```

## Git Bash

```bash
which php
```

Example:

```text
C:\laragon\bin\php\php-8.4.x\php.exe
```

Make sure your terminal is using the PHP version you expect.

---

# 8. Check Composer PHP Version

Composer uses the PHP version available in your terminal.

Run:

```bash
composer diagnose
```

You can also run:

```bash
composer -V
```

If Composer reports a PHP version error, first check:

```bash
php -v
```

---

# 9. Check Node and NPM Location

If you have multiple Node.js versions installed, check which one is being used.

## Windows CMD

```cmd
where node
where npm
```

## Git Bash

```bash
which node
which npm
```

Then verify:

```bash
node -v
npm -v
```

---

# 10. Optional — Use Node Version Manager

If you work with multiple projects that require different Node.js versions, using a Node version manager can make switching versions easier.

Examples:

- NVM
- NVM for Windows
- Volta

For example, with NVM:

```bash
nvm list
```

Then switch Node versions:

```bash
nvm use 24
```

This is optional for beginners.

---

# 11. GitHub SSH Setup

The setup guides in this repository use SSH clone URLs such as:

```bash
git clone git@github.com:laravel/vue-starter-kit.git
```

To use SSH cloning, your GitHub SSH key must already be configured.

You can test your GitHub SSH connection with:

```bash
ssh -T git@github.com
```

If SSH is configured correctly, GitHub should recognize your account.

---

# 12. HTTPS Alternative

If you do not want to configure SSH yet, you can clone using HTTPS.

Example:

```bash
git clone https://github.com/laravel/vue-starter-kit.git
```

Both SSH and HTTPS can be used.

---

# 13. Common Environment Problems

## `php` is not recognized

Example:

```text
'php' is not recognized as an internal or external command
```

Possible reasons:

- PHP is not installed
- PHP is not added to PATH
- Your terminal needs to be restarted

Check your PHP installation and PATH configuration.

---

## `composer` is not recognized

Example:

```text
'composer' is not recognized as an internal or external command
```

Possible reasons:

- Composer is not installed
- Composer is not added to PATH

Install Composer and restart the terminal.

---

## `node` is not recognized

Example:

```text
'node' is not recognized as an internal or external command
```

Install Node.js and restart your terminal.

Then check:

```bash
node -v
npm -v
```

---

## Wrong Node.js Version

Modern Laravel frontend tooling may not work with older Node.js versions.

Check:

```bash
node -v
```

For a new Laravel development environment, use a current LTS version such as:

```text
Node.js 24 LTS
```

---

## Wrong PHP Version

Laravel 13 requires:

```text
PHP >= 8.3
```

Check your version:

```bash
php -v
```

If you have multiple PHP versions installed, check:

```cmd
where php
```

and make sure the correct version is being used.

---

# 14. Recommended Beginner Environment

A simple setup for Windows beginners could be:

```text
Windows 10 / 11
Laragon or Laravel Herd
PHP 8.4+
Composer 2.x
Node.js 24 LTS
NPM
Git
MySQL
VS Code
```

You do not have to use exactly these tools, but this is a practical setup for learning Laravel locally.

---

# 15. Final Checklist

Before continuing to a Laravel setup guide, make sure:

- [ ] PHP 8.3+ installed
- [ ] Composer installed
- [ ] Node.js installed
- [ ] NPM installed
- [ ] Git installed
- [ ] Database available
- [ ] Required PHP extensions enabled
- [ ] `php -v` works
- [ ] `composer -V` works
- [ ] `node -v` works
- [ ] `npm -v` works
- [ ] `git --version` works
- [ ] GitHub SSH works, or you plan to use HTTPS

If everything above is working, you are ready to continue.

---

# Next Step

Choose one of the setup guides:

- [Plain Laravel](./laravel.md)
- [Laravel Vue Starter Kit](./vue-starter-kit.md)
- [Laravel React Starter Kit](./react-starter-kit.md)
- [Laravel Svelte Starter Kit](./svelte-starter-kit.md)
- [Laravel Livewire Starter Kit](./livewire-starter-kit.md)

Happy coding! 🚀
