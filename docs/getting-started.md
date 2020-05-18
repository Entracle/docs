---
id: getting-started
title: Getting started
---
First we need to setup our server to run this Laravel application.
You can visit the official Laravel docs here [Laravel Docs](https://laravel.com/docs) or you can follow this tutorial to setup your server.

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
Entracle uses Laravel Framework as its back end.
Laravel utilises Composer to manage its dependencies. So, before using Laravel, make sure you have composer installed on your machine.
[Install Composer](https://getcomposer.org/download/)


### Step 1: Copy the source code
Unzip the downloaded archive package.
Copy the folder *entracle* to your web server. You should configure your web server’s document / web root to be the public directory (entracle/public). The index.php in this directory serves as the front controller for all HTTP requests entering your application.

Once you have successfully copied the folder, enter that folder and run the command in the terminal to update the project dependencies.
`composer update`

After this is completed you should run this command to update the Application Key for your Laravel project.

```
php artisan key:generate
```


### Step 2: Create an empty database (MySQL)
Create a database for Entracle via your favourite database client.

### Step 3: Configure your environment variables.
You can either visit your website and complete the installation wizard or you can install and configure manually. [Manual Configuration.](bear://x-callback-url/open-note?id=C8E146D2-9C63-4203-9915-F1AED180ADEA-68149-0000AC9826C58FD3)

We’ll first show you how to configure using installation wizard.

If your server is example.com then visit example.com/install and you should see an installation wizard pop up.



Click *Check Requirements* to see if your server matches the installation requirements for Entracle.




You should see all green checks for the PHP Modules required.
Next, click Check Permissions to verify that directories have the correct permissions.


Now that all directories have the correct permissions , let’s configure the environment variables.

You can either choose to follow the wizard or use a text editor to setup the .env file.

If you are familiar with Laravel you can go ahead and configure the .env file as necessary. The only changes that are to be made is specifying the Database details for now.
