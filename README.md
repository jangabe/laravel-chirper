<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

# Bootcamp laravel

## Create a project "chirper" and all docker images (prerequisite is having docker installed)
curl -s "https://laravel.build/chirper" | bash

## The command to start the environment is "./vendor/bin/sail up" inside the chirper folder
create an alias for ./vendor/bin/sail as ->  alias sail='sh $([ -f sail ] && echo sail || echo vendor/bin/sail)'

## Start services docker
Open docker using the new alias -> sail up

## Error: file_put_contents(/var/www/html/storage/framework/views/bae129cef9e600352d1c88ca55b5c61c.php): Failed to open stream: Permission denied
- chmod -R gu+w storage
- chmod -R guo+w storage

## Error: SQLSTATE[42S02]: Base table or view not found: 1146 Table 'laravel.sessions' doesn't exist (Connection: mysql, SQL: select * from `sessions` where `id` = BUP4390325pwQtqJKeTnSODCRDNhmj5dCvYxWQrT limit 1)
sail artisan migrate




