1. Create project inside src folder
 `docker compose run composer create-project --prefer-dist laravel/laravel .`   
<br />


2. edit src/.env database settings
    ```
    DB_CONNECTION=mysql
    DB_HOST=mysql
    DB_PORT=3306
    DB_DATABASE=homestead
    DB_USERNAME=homestead
    DB_PASSWORD=secret
    DB_COLLATION=utf8mb4_unicode_ci
    ```

    Add permission if needed to save changes
    `sudo chmod 666 /path-to-project/src/.env`
<br />

3. Start services
`docker compose up -d server php mysql`
<br />

4. Run artisan migration
    `docker compose run artisan migrate`
<br />

5. Visit laravel app http://localhost:8000/