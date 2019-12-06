FROM php:7.4.0
RUN apt-get update && apt-get install -y unzip sqlite3 composer \
	&& docker-php-ext-install bcmath pcntl
