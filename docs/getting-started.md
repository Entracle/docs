---
id: getting-started
title: Getting started
---

You can visit the official Laravel docs here [Laravel Docs](https://laravel.com/docs) or you can follow this tutorial to setup your server.

<img alt="Docusaurus campfire" src="/img/undraw_monitor.svg" class="docImage"/>

## Server Requirements
* PHP >= 7.2.5
* BCMath PHP Extension
* Ctype PHP Extension
* Fileinfo PHP extension
* JSON PHP Extension
* Mbstring PHP Extension
* OpenSSL PHP Extension
* PDO PHP Extension
* Tokenizer PHP Extension
* XML PHP Extension

## Installing
Entracle uses Laravel Framework as its back-end.
Laravel utilises Composer to manage its dependencies.

So, before using Laravel, make sure you have composer installed on your machine.
[Install Composer](https://getcomposer.org/download/)

#### Need help setting up a webserver before you configure entracle?
If you already have a webserver setup then you can skip to the next step.
[Server setup tutorial DigitalOcean]('https://sd')

### Step 1: Copy the source code
Unzip the downloaded archive package.


Copy the folder *entracle* to your web server. You should configure your web server’s document / web root to be the public directory which is  `entracle\public`

Once you have successfully copied the folder, go into that folder and run the command in the terminal to update the project dependencies.
```sh
composer update
```

After this is completed you should run this command to update the Application Key for your Laravel project.

```sh
php artisan key:generate
```


### Step 2: Create an empty database (MySQL)
Create a database for Entracle via your favourite database client.

### Step 3: Configure your environment variables.
You can either visit your website and complete the installation wizard or you can install and configure manually. [Manual Configuration.](bear://x-callback-url/open-note?id=C8E146D2-9C63-4203-9915-F1AED180ADEA-68149-0000AC9826C58FD3)

#### Configure using installation wizard.

If your server is example.com then visit example.com/install and you should see an installation wizard pop up.



Click *Check Requirements* to see if your server matches the installation requirements for Entracle.




You should see all green checks for the PHP Modules required.
Next, click Check Permissions to verify that directories have the correct permissions.


Now that all directories have the correct permissions , let’s configure the environment variables.

You can either choose to follow the wizard or use a text editor to setup the .env file.

#### Configure Manually
If you are familiar with Laravel you can go ahead and configure the .env file as necessary. The only changes that are to be made is specifying the Database details for now.

You need to change the `DB_DATABASE`, `DB_USERNAME` & `DB_PASSWORD`
to what you created in [here](#step-2-create-an-empty-database-mysql).
The host and port remains the same for most of the cases.

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=yourdatabasename
DB_USERNAME=yourdatabaseusername
DB_PASSWORD=yourpassword
```



## Migrating & Seeding the Database

Once you've set up your server and installed the dependencies, its time to migrate the database and seed the essential data first.

#### Open up terminal in project root directory and run
```sh
php artisan migrate:refresh --seed
```

You should see a similar success message in your console.

`Database seeding completed successfully.
`

#### That's it. You've successfully setup your server, go and check it out.

Visit your website / and you should see the entracle landing page.
