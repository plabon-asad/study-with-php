# Study with PHP and Laravel
Study for self development to be a PHP (Laravel) developer.

## Deployment [Link](https://learnwith.polashmahmud.com/courses/deploy-laravel-and-vue-js-project-with-linux-server-(vps))
### Requirements
- Install os(Linux: ubuntu)
- Install ngnix, DB server
- Install language (PHP, all package that are needed)
- Install composer and config
- Install git and add ssh_public_key

### Server Management
- Root user (all permission)
- Create new user (specific permission)

- Login server and then Add user `adduser user_name`
- Login to new_user from root_user `su user_name` and check `pwd`
- ssh-key add `ssh-keygen`

- Ngnix: default user update by myself_user
- Goto config file `nano /etc/ nginx/nginx.conf` and default user is: `www-data`. Update it by `myself_user` then save it and restart ngnix `service ngnix restart`

- Make directory for all project like **laravel** or **vue**


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

Certainly! Laravel provides a rich set of query builder methods that allow you to interact with your database in a convenient and expressive way. Here are some commonly used query builder methods in Laravel:

**Selecting Columns:**
- `select('column1', 'column2')`: Specify columns to be retrieved.
- `addSelect('column3')`: Add additional columns to the select clause.

**Filtering Results:**
- `where('column', 'value')`: Basic where clause.
- `orWhere('column', 'value')`: Or where clause.
- `whereBetween('column', [$start, $end])`: Where between a range.
- `whereIn('column', [value1, value2])`: Where in an array of values.
- `whereNull('column'), whereNotNull('column')`: Check for null or not null values.
- `whereDate('column', '2022-01-01')`: Filter by date.
- `whereRaw('column = ?', [$value])`: Raw where clause.

**Ordering Results**:
- `orderBy('column', 'asc')`: Order by a column in ascending or descending order.
- `latest(), oldest()`: Order by the created_at or updated_at columns.

**Joining Tables:**
- `join('table', 'table.column', '=', 'other_table.column')`: Inner join.
- `leftJoin('table', 'table.column', '=', 'other_table.column')`: Left join.
- `rightJoin('table', 'table.column', '=', 'other_table.column')`: Right join.

**Grouping and Aggregates:**
- `groupBy('column')`: Group results by a column.
- `count(), sum('column'), avg('column')`: Aggregate functions.

**Eager Loading Relationships:**
- `with('relation')`: Eager load relationships to avoid N+1 query issues.
- `withCount('relation')`: Load relationship counts.

**Inserting and Updating:**
- `insert(['column' => 'value'])`: Insert a new record.
- `update(['column' => 'new_value'])`: Update records.

**Deleting Records:**
- `delete()`: Delete records.

**Pagination**:
- `paginate($perPage)`: Paginate the results.

**Other Methods:**
- `distinct()`: Return only distinct results.
- `limit($count)`: Limit the number of results.
- `get()`: Retrieve the results.

These are just a few examples of the many methods available in Laravel's query builder. Laravel's documentation provides extensive information on each of these methods, including examples and use cases. You can refer to the official documentation for more details: Laravel Query Builder.
