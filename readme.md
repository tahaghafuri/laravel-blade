### Installation

```
composer require tahaghafuri/blade
```
### Usage

```php
<?php

/*
|--------------------------------------------------------------------------
| Register The Auto Loader
|--------------------------------------------------------------------------
|
| Composer provides a convenient, automatically generated class loader
| for our application. We just need to utilize it! We'll require it
| into the script here so that we do not have to worry about the
| loading of any our classes "manually". Feels great to relax.
|
*/

require __DIR__.'/vendor/autoload.php';

use TAG\Blade\Blade;
use Illuminate\Events\Dispatcher;

$views = __DIR__ . '/views';
$cache = __DIR__ . '/cache';

$blade = new Blade($views, $cache, new Dispatcher);
echo $blade->view()->make('hello')->render();
