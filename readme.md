## DBug

**laravel-5-dbug** is a Laravel package that makes your variable dumps look nicer with the [ospintos dBug class](https://github.com/ospinto/dbug). The output is comparable to ColdFusion's cfdump. This repository is a fork from [dlcrush/laravel-dbug](https://github.com/dlcrush/laravel-dbug) with an update for Laravel 5 and a few minor fixes.

## Installation

This will walk you through how to set up the package.

1. Add the following to your composer.json under require and then run `composer update`

`"repat/laravel-5-dbug": "~1.*"`

OR 

`composer require repat/laravel-5-dbug`


2 Add the Service Provider to the providers array in `app/config/app.php`

```php
dlcrush\DBug\DBugServiceProvider::class,
```

4) Add alias in `app/config/app.php`

```php
'DBug'			  => dlcrush\DBug\Facades\DBug::class,
```

### Usage

To dump out a variable, do the following:

```php
DBug::DBug($var);
```

To dump and then die, do the following:

```php
DBug::DBug($var, true);
```
