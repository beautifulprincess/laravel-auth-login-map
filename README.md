### Installation Instructions
1. Run `sudo git clone https://github.com/jeremykenedy/laravel-auth.git laravel-auth`
2. Create a MySQL database for the project
    * ```mysql -u root -p```, if using Vagrant: ```mysql -u homestead -psecret```
    * ```create database laravelAuth;```
    * ```\q```
3. From the projects root run `cp .env.example .env`
4. Configure your `.env` file // NOTE: Google API Key will prevent maps error
5. Run `sudo composer update` from the projects root folder
6. Run `php artisan vendor:publish --provider="jeremykenedy\LaravelRoles\RolesServiceProvider" --tag=config`
7. Run `php artisan vendor:publish --provider="jeremykenedy\LaravelRoles\RolesServiceProvider" --tag=migrations`
8. Run `php artisan vendor:publish --provider="jeremykenedy\LaravelRoles\RolesServiceProvider" --tag=seeds`
9. From the projects root folder run `sudo chmod -R 755 ../laravel-auth`
10. From the projects root folder run `php artisan key:generate`
11. From the projects root folder run `php artisan migrate`
12. From the projects root folder run `composer dump-autoload`
13. From the projects root folder run `php artisan db:seed`
