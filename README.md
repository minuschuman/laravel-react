# Laravel-React

## Pre-requisites
- PHP 8 or higher
- Composer
- NPM
- MySQL

## Installation
installing laravel
```bash
composer create-project --prefer-dist laravel/laravel ./
```

install the inertiajs
```bash
composer require inertiajs/inertia-laravel
```

add new blade file in resources/views/app.blade.php
```bash
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Laravel</title>
        @viteReactRefresh 
        @vite(['resources/css/app.css', 'resources/js/app.jsx'])
        @inertiaHead
    </head>
    <body>
        @inertia
    </body>
</html>
```

generate middleware for inertia
```bash
php artisan inertia:middleware
```

add to the middleware group app/Http/Kernel.php
```bash
'web' => [
    // ...
    \App\Http\Middleware\HandleInertiaRequests::class,
],
```

npm install
```bash
npm install
```

install react
```bash
npm install react react-dom@latest
```

install vite
```bash
npm install @vitejs/plugin-react
npm install @vitejs/plugin-react-refresh
```
install inertia react
```bash
npm install @inertiajs/inertia-react @inertiajs/react  
```
