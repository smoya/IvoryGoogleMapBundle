# UPGRADE

### 1.0.0 to 2.0.0

The business classes have been moved to a dedicated library for reuasibility purpose. If you're using Symfony 2.0.*,
you need to update your `deps` file:

```
[ivory-google-map]
    git=http://github.com/egeloen/ivory-google-map.git
```

Autoload the library:

``` php
// app/autoload.php

$loader->registerNamespaces(array(
    'Ivory\\GoogleMap' => __DIR__.'/../vendor/ivory-google-map/src',
    // ...
);
```

Run the vendors script:

``` bash
$ php bin/vendors update
```
