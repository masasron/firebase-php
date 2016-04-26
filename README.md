# Firebase PHP Client

### Installation

The recommended way to install Firebase is through [Composer](http://getcomposer.org).

```bash
composer require masasron/firebase-php dev-master
```

### Quick usage example

```php
$firebase = new \Firebase\Client('https://test123.firebaseio.com');

$firebase->set([ 'messages' => [] ]);

$messagesRef = $firebase->child('/messages');

$messagesRef->push('Foo');
$messagesRef->push('Bar');
$messagesRef->push('Hello World');
```

### Authentication

```php
$token = 'TOKEN_IN_HERE';

$firebase = new \Firebase\Client('https://test123.firebaseio.com',$token);

$firebase->child('/users/ron/email').set('ron@test.com');
```

### Other

```php
// Set
$firebase->child('/users/ron')->set([ 'id' => 1,'name' => 'Ron' ]);

// Update
$firebase->child('/users/ron/name')->set('Ronald');

// Push
$liks = $firebase->child('/users/ron/liks');
$liks->push('PHP');
$liks->push('Firebase');

// Get
$user = $firebase->child('/users/ron')->get();

// Delete
$firebase->child('/users/ron')->delete();
```


