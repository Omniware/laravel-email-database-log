# Laravel Email Database Log

A simple database logger for all outgoing emails sent by Laravel website.

## Installation

Laravel Email Database Log can be installed via [composer](http://getcomposer.org) by requiring the `omniware/laravel-email-database-log` package in your project's `composer.json`.

```json
{
    "require": {
        "omniware/laravel-email-database-log": "*"
    }
}
```

Next add the service provider and the alias to `app/config/app`.

```php
'providers' => [
    // ...
    Omniware\LaravelEmailDatabaseLog\LaravelEmailDatabaseLogServiceProvider::class,
],
```


Now, run this in terminal:

```bash
php artisan vendor:publish --provider="Omniware\LaravelEmailDatabaseLog\LaravelEmailDatabaseLogServiceProvider" --tag="migrations"

php artisan migrate
```

## Usage

After installation, any email sent by your website will be logged to `email_log` table in the site's database.
