# Laravel Setup Guides

Beginner-friendly setup guides for creating Laravel projects directly from the official Laravel GitHub repositories.

These guides are useful when:

- `laravel new project-name` does not work correctly
- Composer or network issues prevent Laravel Installer from completing
- You want to start directly from an official Laravel Starter Kit
- You want a simple step-by-step setup guide
- You are learning Laravel for the first time

---

## Available Setup Guides

Choose the Laravel project you want to use.

### 1. Plain Laravel

Basic Laravel project without a frontend starter kit.

👉 [Laravel Setup Guide](./laravel.md)

Official Repository:

https://github.com/laravel/laravel

---

### 2. Laravel Vue Starter Kit

Laravel with Vue, Inertia, Tailwind CSS and authentication.

👉 [Vue Starter Kit Setup Guide](./vue-starter-kit.md)

Official Repository:

https://github.com/laravel/vue-starter-kit

---

### 3. Laravel React Starter Kit

Laravel with React, Inertia, Tailwind CSS and authentication.

👉 [React Starter Kit Setup Guide](./react-starter-kit.md)

Official Repository:

https://github.com/laravel/react-starter-kit

---

### 4. Laravel Svelte Starter Kit

Laravel with Svelte, Inertia, Tailwind CSS and authentication.

👉 [Svelte Starter Kit Setup Guide](./svelte-starter-kit.md)

Official Repository:

https://github.com/laravel/svelte-starter-kit

---

### 5. Laravel Livewire Starter Kit

Laravel with Livewire, Tailwind CSS and authentication.

👉 [Livewire Starter Kit Setup Guide](./livewire-starter-kit.md)

Official Repository:

https://github.com/laravel/livewire-starter-kit

---

# Before You Start

Before following any of the setup guides, make sure your development environment is ready.

You will need:

- PHP
- Composer
- Node.js
- NPM
- Git
- A database such as MySQL, PostgreSQL or SQLite

👉 [Environment Setup & Requirements](./environment-setup.md)

You can quickly check your environment with:

```bash
php -v
composer -V
node -v
npm -v
git --version
```

If all of these commands work correctly, you are ready to continue.

---

# Project Structure

```text
laravel-setup-guides/
├── README.md
├── environment-setup.md
├── laravel.md
├── vue-starter-kit.md
├── react-starter-kit.md
├── svelte-starter-kit.md
└── livewire-starter-kit.md
```

---

# Which One Should I Choose?

If you are not sure which Laravel project to use:

| Project | Recommended For |
|---|---|
| Plain Laravel | Learning Laravel backend and Blade from scratch |
| Vue Starter Kit | Laravel + Vue full-stack development |
| React Starter Kit | Laravel + React full-stack development |
| Svelte Starter Kit | Laravel + Svelte full-stack development |
| Livewire Starter Kit | Laravel full-stack development with PHP-first approach |

For absolute beginners learning Laravel itself, starting with **Plain Laravel** is usually easier.

If you already understand Laravel basics and want to build a modern SPA-style application, choose Vue, React or Svelte.

If you prefer to stay mostly inside Laravel and PHP, Livewire is a good option.

---

# General Setup Flow

Although each project is slightly different, the general setup process is usually:

```text
1. Clone the official Laravel repository
2. Enter the project directory
3. Remove the existing Git history
4. Initialize your own Git repository
5. Install Composer dependencies
6. Create the .env file
7. Generate the application key
8. Configure the database
9. Run database migrations
10. Install frontend dependencies
11. Start the development servers
```

Each guide explains these steps in more detail.

---

# Important

These projects are cloned directly from the official Laravel repositories.

After cloning, the guides will normally ask you to remove the existing `.git` directory:

```bash
rm -rf .git
```

and initialize a fresh Git repository:

```bash
git init
```

This removes the Laravel repository's Git history and lets you start your own project history.

> Removing `.git` does not delete your Laravel project files. It only removes the existing Git repository information.

---

# Development Servers

For most Laravel projects, you will normally run two development servers.

### Laravel

```bash
php artisan serve
```

### Frontend

```bash
npm run dev
```

Laravel normally runs at:

```text
http://127.0.0.1:8000
```

---

# Who Is This For?

These guides are designed mainly for:

- Laravel beginners
- Students
- Bootcamp learners
- Developers using Windows or Laragon
- Developers who have trouble using Laravel Installer
- Anyone who wants a simple Laravel project setup reference

The goal is to keep every guide simple, practical and beginner-friendly.

---

# Official Laravel Resources

Laravel Documentation:

https://laravel.com/docs

Laravel GitHub:

https://github.com/laravel

Laravel Starter Kits:

https://laravel.com/starter-kits

---

# Note

Laravel and its starter kits may change over time.

If you encounter dependency or version issues, always check:

```bash
php -v
composer -V
node -v
npm -v
```

and compare your environment with:

👉 [Environment Setup & Requirements](./environment-setup.md)

---

## License

This repository contains setup guides and learning notes.

Laravel itself is open-source software licensed under the MIT License.

---

Happy coding! 🚀
