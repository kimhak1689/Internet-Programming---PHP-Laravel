FROM lorisleiva/laravel-docker:7.3
EXPOSE 9111

COPY .  /var/www
RUN rm -f composer.lock
RUN composer install
RUN cp .env.example .env
RUN php artisan key:generate

CMD php artisan --host=0.0.0.0 serve --port=9111