---
title: How to Laravel
date: 2025-06-10 17:00:00 +0000
categories: [blog, PHP]
tags: [Blog, technical, mazepin, PHP]
---

# How to Laravel

## We need:

[PHP](https://www.php.net/downloads)

[Nodejs](https://nodejs.org/en) + npm

[Composer](https://getcomposer.org/): 
`composer create-project laravel/laravel example-app`

For local dev work use: [Laravel Herd](https://herd.laravel.com/)

Frontend Docu: [LaravelDOC](https://laravel.com/docs/11.x/frontend)

## Basic functionality:

- **App**: Dieser Ordner enthält den Hauptcode Ihrer Anwendung, einschließlich Models, Controllers, und Middleware.
- **Controllers**: Führen den php code aus und verarbeiten daten
- **Models**: zentrale Quelle für die Interaktion mit Datenbanken dienen.
- **Middelware**: HTTP-Anfragen filtert und bearbeitet, bevor sie die Anwendung erreichen, sowie Antworten, bevor sie an den Client zurückgesendet werden.

- **Config**: Dieser Ordner enthält alle Konfigurationsdateien der Anwendung. Default configs are in /.env. Wenn änderung laravel server neustarten
- **Database**: Hier finden Sie Migrationen, Datenbank-Seed-Dateien, und die SQLite-Datenbankdatei.

- **public**: Dieser Ordner enthält die index.php Datei, die als Einstiegspunkt für alle Anfragen dient. Hier können auch Ihre öffentlich zugänglichen Assets wie Bilder, JavaScript- und CSS-Dateien gespeichert werden. Die Kompilierten js Dateien sind hier

- **Resources**: views für html pages, sollte app.balde verwenden
- **Blade**: für templasetes header menu etc: unter resources/views/layouts/app.balde.php
- **Routes**: Alle Routen-Dateien der Anwendung befinden sich hier.
- **Storage**: Hier werden kompilierte Blade-Templates, Dateien, Sitzungen und andere vom Framework generierte Dateien gespeichert.
- **Artisan**: show help with “php artisan”; php artisan migrate for writing fresh to db

## Tinker:

Mit php artisan tinker können wir mit der app über cli interagieren. Z.b mit `User::all();` kann man sich alle User mit den dazugehörigen infos anzeigen lassen.

## Start Laravel Application:

`sudo composer install`- To install dependecies

`php artisan server` - Starts server on 127.0.0.1:8000

npm install, `npm run dev`

## Deploy on Ubuntu Server:

[https://www.youtube.com/watch?v=fpGXm2eVTNw](https://www.youtube.com/watch?v=fpGXm2eVTNw)

**Install Required Packages**:

`sudo apt install apache2 mysql-server php php-mysql libapache2-mod-php php-cli php-zip php-  xml php-mbstring php-curl git unzip`

**Install Composer**:
`curl -sS [https://getcomposer.org/installer](https://getcomposer.org/installer) | php`

`sudo mv composer.phar /usr/local/bin/composer`

**Clone Laravel Project**:
`cd /var/www/html`

`sudo git clone <your-repo-url> projectname`

`cd projectname`

**Install Laravel Dependencies**:
`sudo composer install`

**Set Permissions**:
`sudo chown -R www-data:www-data /var/www/html/projectname`
`sudo chmod -R 775 /var/www/html/projectname/storage`

`sudo chmod -R 775 /var/www/html/projectname/bootstrap/cache`

**Set Up Apache Virtual Host**:
`sudo nano /etc/apache2/sites-available/laravel.conf`

folgendes einfügen:

```yaml
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/html/projectname/public

    <Directory /var/www/html/projectname>
        AllowOverride All
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

**Enable Apache Modules and Site**:
`sudo a2enmod rewrite`
`sudo a2ensite laravel.conf`

`sudo systemctl restart apache2`