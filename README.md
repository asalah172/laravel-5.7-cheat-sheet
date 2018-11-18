# Laravel 5.7 Cheat Sheet
This is a full summary of  the `Laravel` documentation.

-----
## Routing

###### Basic route syntax using closure function
```php
Route::get('foo', function () {
    return 'Hello World';
});
```
---
###### Basic route syntax calling a controller method
```php
Route::get('/user', 'UserController@index');
```
---
###### Available Router Methods
```php
Route::get($uri, $callback);
Route::post($uri, $callback);
Route::put($uri, $callback);
Route::patch($uri, $callback);
Route::delete($uri, $callback);
Route::options($uri, $callback);
```
---
###### A route that responds to multiple HTTP verbs
```php
Route::match(['get', 'post'], '/', function () {
    //
});

Route::any('foo', function () {
    //
});
```
---
###### CSRF Blade Snippet
```blade
@csrf
```
---
###### Redirect Routes
```php
Route::redirect('/here', '/there', 301);
```

---
###### View Routes
```php
Route::view('/welcome', 'welcome');

Route::view('/welcome', 'welcome', ['name' => 'Taylor']);
```
