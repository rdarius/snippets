# PHP
[PHP - CORS](https://github.com/rdarius/snippets/tree/master/php/cors)


# Settings

## Cahnge Memory Limit
```php
ini_set('memory_limit', '256M'); // set the limit
ini_set('memory_limit', '-1'); // remove limits
```
---
## Display All Errors
```php
ini_set('display_errors', 1);
ini_set('display_startup_errors', 1);
error_reporting(E_ALL);
```
---
## Change execution time limit
```php
set_time_limit(360000);
```
---
## CORS
```php
/* Handle CORS */

// Specify domains from which requests are allowed
header('Access-Control-Allow-Origin: *');

// Specify which request methods are allowed
header('Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS');

// Additional headers which may be sent along with the CORS request
header('Access-Control-Allow-Headers: X-Requested-With,Authorization,Content-Type');

// Set the age to 1 day to improve speed/caching.
header('Access-Control-Max-Age: 86400');

// Exit early so the page isn't fully loaded for options requests
if (strtolower($_SERVER['REQUEST_METHOD']) == 'options') {
    exit();
}
```
