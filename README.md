# Cachet Badger

A badge generator for Laravel 8.


## Installation

This version requires [PHP](https://php.net) 7.1 - 8.0, and supports Laravel 8 and above.

To get the latest version, simply require the project using [Composer](https://getcomposer.org):

```bash
$ composer require rafaelmoresco/badger
```

Once installed, if you are not using automatic package discovery, then you need to register the `CachetHQ\Badger\BadgerServiceProvider` service provider in your `config/app.php`.


## Examples


Get started immediately:

```php
// Using the facade
Badger::generate('license', 'MIT', 'blue', 'plastic')

// Dependency injection example
$badger->generate('license', 'MIT', '#ff69b4', 'plastic')
```

![License Blue MIT](https://cdn.rawgit.com/CachetHQ/Badger/master/tests/stubs/license-MIT-blue-plastic.svg)
![License Custom MIT](https://cdn.rawgit.com/CachetHQ/Badger/master/tests/stubs/license-MIT-custom-plastic.svg)


## Usage

The generate method takes four parameters:

```php
Badger::generate('license', 'MIT', 'blue', 'flat-square')
```

The first parameter is the subject, or what it is the badge is showing. In the example above this is the license. The second parameter is the value (the right hand of the badge). Next is the color of the badge. This can be one of the following preset colors _or_ a valid hex string.

- `brightgreen`
- `green`
- `yellow`
- `yellowgreen`
- `orange`
- `red`
- `blue`
- `grey`
- `lightgray`

And finally the fourth parameter is the badge type. This determines the style of the badge and can be one of the four values below.

- `flat-square` (default)
- `plastic-flat`, `flat`
- `plastic`
- `social` (without links)


## Security

If you discover a security vulnerability within this package, please e-mail us at support@cachethq.io. All security vulnerabilities will be promptly addressed.


## License

Cachet Badger is licensed under [The MIT License (MIT)](LICENSE).

Based on the work done at [badges/poser](https://github.com/badges/poser).
