# Clear-cache-in-Laravel-5
This is how to clear cache in Laravel 5
---
## **Clear Cache in Laravel (Terminal)**
Log in to the system running you Laravel application and open a terminal. Then navigate to your Laravel application code. Here you can issue the commands to clear cache as followings:

**1. Clear Application Cache **
Run the following command to clear application cache of the Laravel application.
```
php artisan cache:clear
```

**2. Clear route cache **
To clear route cache of your Laravel application execute the following command from the shell.
```
php artisan route:cache
```

**3. Clear config cache **
You can use config:cache to clear the config cache of the Laravel application.
```
php artisan config:cache  
```

**4. Clear compiled view files **
Also, you may need to clear compiled view files of your Laravel application. To clear compiled view files run the following command from the terminal.
```
php artisan view:clear 
```

## **Clear Cache in Laravel (Browser)**
Most of the shared hosting providers don’t provide SSH access to the systems. In that case, you can clear Laravel cache by calling URL in the browser. You can simply place the below code in your routes/web.php file of Laravel application. Then access this URL in the browser to clear the cache of Laravel application.
```php
Route::get('/clear-cache', function() {
    Artisan::call('cache:clear');
    return "Cache is cleared";
});
```
