FROM php:latest

RUN pecl install swoole

RUN docker-php-ext-enable swoole

EXPOSE 80

ENTRYPOINT exec php /var/www/artisan swoole:http start && tail -f /var/www/storage/logs/*