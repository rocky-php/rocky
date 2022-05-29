# Simyo

A minimal PSR-7 / PSR-15 application. 

## Requirements

* PHP 7.4+

## Installation

```
composer create-project odan/simyo my-app
```

## Performance

Run: `composer update --no-dev -o`

Disable XDebug in php.ini

```ini
[XDebug]
;zend_extension=xdebug
```

Restart the webserver.

Command to test the performance: `ab -n 5000 -c 10 -k http://localhost/simyo/`

Requests per seconds (more is better):

* Vanilla PHP: 5240
* FastRoute: 1054
* **This project with FastRoute: 437**
* Slim 4 demo: 415
* This project with symfony/routing: 347
* This project with league/route: 204
* odan/slim4-skeleton: 182

## License

The MIT License (MIT).
