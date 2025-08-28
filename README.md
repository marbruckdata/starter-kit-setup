# starter-kit-setup

### Create Laravel 11 project
- composer create-project laravel/laravel example-app 11
- cd example-app

### Server-Side Inertiajs
- composer require inertiajs/inertia-laravel
- root template see "app.blade.php"

### Inertiajs Middleware (Laravel 11)
- php artisan inertia:middleware
- check bootstrap/app.js

### Setup Controller, Route, and Vue template
- php artisan make:controller HomeController
- check web.php for route
- check Home.vue for template
- check HomeController.php
- npm install
- npm run dev

### Frontend Inertiajs
- npm install @inertiajs/vue3
- check resources/js/app.js
- npm i @vitejs/plugin-vue (optional???)
- check vite.config.js

### Install TailwindCSS
- npm install tailwindcss @tailwindcss/vite
- check vite.config.ts
- check ./resources/css/app.css
- check app.blade.php

### Install Tailwind Forms
- npm install -D @tailwindcss/forms
- check app.css

### Install Fortify
- composer require laravel/fortify
- php artisan fortify:install
- php artisan migrate
- set config/fortify views=>false

  
