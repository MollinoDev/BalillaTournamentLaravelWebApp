# What this site does
WebSite that visualizes the result of a goal counter for a Calcio Balilla Tournament (alias "Biliardino") 

# Make it works properly locally

## project structure

1. create a folder named "BalillaTournamentWebSite" and inside it 2 folder: "include" and "laravelApp"
2. inside include create "connect.php" file, open it an paste:
```
<?php 
$APP_URL="http://localhost";
$USER="root";
$DB="mollinodb";
$HOST="127.0.0.1";
$PASSWORD="root";
```
3. open a terminal inside laravelApp and run ```git clone https://github.com/MollinoDev/BalillaTournamentLaravelWebApp.git```

Now you should have this structure:
- BalillaTournamentWebSite
    - include
        - connect.php
    - laravelApp
        - ...

## apache
Be sure you are currently running your apache server. 
4. Go to localhost/phpMyAdmin5/ on your browser and create a new db named "mollinodb"

## composer
5. Open a terminal inside the laravelApp and run these commands:

    ```composer install```
    ```cp .env.example .env```
    ```php artisan key:generate```
    ```chmod 755 storage -R```
    ```chmod 755 public -R```
    
## migration and seed
6. run these commands:
    ```composer update```
    ```php artisan migrate:fresh```
    ```php artisan db:seed```
7. Go to localhost and inside your public folder. The site shoul work!
