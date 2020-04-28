# Laravel Query Monitor

<a href="https://packagist.org/packages/supliu/laravel-query-monitor"><img src="https://poser.pugx.org/supliu/laravel-query-monitor/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/supliu/laravel-query-monitor"><img src="https://poser.pugx.org/supliu/laravel-query-monitor/v/stable.svg" alt="Latest Stable Version"></a>

<a href="https://supliu.com.br">Supliu</a> Laravel Query Monitor is library to monitoring Queries in real-time using Laravel Artisan Command. Basically it opens a socket listening and displays (on terminal) the queries executed in your Laravel application.

<p align="center">
  <img src="demo.gif" width="100%">
</p>


## How to install

Use composer to install this package

```
composer require --dev supliu/laravel-query-monitor
```

## How to use

Open you terminal and execute:

```ssh
php artisan laravel-query-monitor
```

Now just perform some action in your application that performs some interaction with the database.

## Custom

By default, the query listening service will run on host 0.0.0.0 and port 8081. You can customize both the host and the port by providing the optional arguments:

```ssh
php artisan laravel-query-monitor --host="192.168.0.2" --port=8082
```

If you change the host and port parameters, you will also need to change the configuration file `config/laravel-query-monitor.php`. To edit it, you must first publish the package:

```ssh
php artisan vendor:publish --provider="Supliu\LaravelQueryMonitor\ServiceProvider"
```



## License

The Laravel Query Monitor is open-sourced project licensed under the [MIT license](https://opensource.org/licenses/MIT).
