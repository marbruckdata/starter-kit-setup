# starter-kit-setup

### Create Laravel 11 project
- composer create-project laravel/laravel example-app 11
- cd example-app

### Server-Side Inertiajs
- composer require inertiajs/inertia-laravel
- root template see "app.blade.php"
```php
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    @inertiaHead
    @vite(['resources/css/app.css', 'resources/js/app.js'   ])
</head>
<body>
@inertia

</body>
</html>
```

### Inertiajs Middleware (Laravel 11)
- php artisan inertia:middleware
- check bootstrap/app.js

```php
<?php

use App\Http\Middleware\HandleInertiaRequests;
use Illuminate\Foundation\Application;
use Illuminate\Foundation\Configuration\Exceptions;
use Illuminate\Foundation\Configuration\Middleware;

return Application::configure(basePath: dirname(__DIR__))
    ->withRouting(
        web: __DIR__.'/../routes/web.php',
        commands: __DIR__.'/../routes/console.php',
        health: '/up',
    )

    // EDIT THIS HERE START
    ->withMiddleware(function (Middleware $middleware) {
        $middleware->web(append:[HandleInertiaRequests::class]);
    })
    // EDIT THIS HERE END

    ->withExceptions(function (Exceptions $exceptions) {
        //
    })->create();
```

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

  
