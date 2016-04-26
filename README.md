# Firebase PHP Client

### Installation

The recommended way to install Firebase is through [Composer](http://getcomposer.org).

```bash
composer require masasron/firebase-php dev-master
```

### Quick usage example

```php

$firebase = new \Firebase\Client('https://test123.firebaseio.com');

$firebase->set([ 'message' => [] ]);

$ref = $firebase->child('/message');

$ref->push([
    'from' => 'me',
    'message' => 'Hello!'
]);

print_r($ref->get());

```
