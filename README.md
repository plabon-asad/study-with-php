# Study with PHP and Laravel
Study for self development to be a PHP (Laravel) developer.

# Pre Requirements to config Laravel (Windows11)
 - Xampp install (Apache, Mysql)
 - PG install with PG Admin
 - Composer install
 - Make laravel global by composer
 - Make laravel project and run

| Link | Description |
| ------ | ------ |
| [See here](https://stackoverflow.com/questions/45790160/is-there-way-to-use-two-php-versions-in-xampp) | How to manage multiple version PHP in Windows 11 by XAMPP |
| [Naming Convention](https://webdevetc.com/blog/laravel-naming-conventions) | Laravel Naming Convention |
| [Best Practices](https://github.com/alexeymezenin/laravel-best-practices#follow-laravel-naming-conventions) | Laravel Best Practices |
| [Laravel Storage](https://medium.com/p/33b66cfa8c2c) | Laravel storage guide |


❗Some important keywords of Laravel - 
`Eloquent`, `Blade`, `Middlewire`, `Livewire`, `Vite`, `Breeze`

### 🔰Eloquent: ### 
ORM(Object Relational Map)

### 🔰Blade: ### 
Blade is the simple, powerful templating engine that is included with Laravel. Blade does not restrict you from using plain PHP code in your templates. In fact, all Blade templates are compiled into plain PHP code and cached until they are modified. 
<br>Extension: `.blade.php` 
<br>Typically stored directory `resources/views`

There are two primary ways to tackle frontend development when building an application with Laravel,

### 🔰Reserved Keywords: ###
By default, some keywords are reserved for Blade's internal use in order to render components.<br>
`data`, `render`, `resolveView`, `shouldRender`, `view`, `withAttributes`, `withName`


## ❌ Error List ##
| ❗Error | ✅Solution | Description |
| ------ | ------ |------ |
| XAMPP - [Shutdown MySql](https://i.stack.imgur.com/j8ntw.png) | [See here](https://i.stack.imgur.com/uyvBO.png) | To learn PHP and Laravel I stucked many times for many kind of issues. Here `MySql` crushed sudden. [See Details](https://stackoverflow.com/questions/18022809/how-to-solve-error-mysql-shutdown-unexpectedly) |

Some Basic Commands
| Description | Command |
| ------ | ------ |
| Run Laravel project | `php artisan serve` with port `php artisan serve --port=8080` |
| About project | `php artisan about`, only interested in a particular section of the application overview `php artisan about --only=environment` |
| Enable/Disabling Maintenance Mode | `php artisan down` `php artisan up` |
| All available Artisan commands  | `php artisan list` |
| Laravel Console  | `php artisan tinker` |
| Migration  | `php artisan migrate` |
| Rollback Migration  | `php artisan migrate:rollback`, rollback with step `php artisan migrate:rollback --step=5`, full rollback `php artisan migrate:reset` |


