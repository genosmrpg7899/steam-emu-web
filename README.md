# Steam Server Emulator Web [![Discord Invite](https://discordapp.com/api/guilds/1095748820748488848/widget.png?style=shield)](https://discord.gg/3fhdb2YvZV)
A dynamic web setup for shefben's fork of pmein1's Steam Server Emulator written in the Laravel 10 framework

# Requirements
- A web server of your choice (I personally use apache for this)
- A MySQL-based database provider (I personally use MariaDB)
- [PHP 8.2+](https://www.php.net/downloads)
- [Composer](https://getcomposer.org/)
- [The emulator itself](https://github.com/shefben/stmsrvemu)

# Usage
- Make sure you have composer installed in your PATH, and linked it to your PHP installation in the setup.
- Clone this repo, and navigate to the root path of the project in your system's command line.
- Run `composer install` to install all of the project's dependencies.
- Configure your webserver accordingly to the [official Laravel documentation](https://laravel.com/docs/10.x/deployment).
  - Note that an .htaccess is already provided in the /public folder so simply setting a DocumentRoot in your Apache configuration will work.
- Configure your database provider and create a new database whether from phpmyadmin or the command line, and modify the project's .env file (located in root) to connect to the database.
- Once database and .env are configured as per the previous steps, run `php artisan migrate`. It will tell you the status of importing each database migration in realtime.
