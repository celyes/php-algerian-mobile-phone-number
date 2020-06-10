# Algerian mobile phone number value object

Algerian mobile phone number value object implementation that can be used in your domain models or to integrate with your favorite framework.

## Installation

```
composer require cherif/algerian-mobile-phone-number
```

## Usage:

### Instantiation:

The class doesn't have a public constructor, it has a named constructor instead in order to preseve its invariants:

```php
use Cherif\AlgerianMobilePhoneNumber\AlgerianMobilePhoneNumber;

$phoneNumber = AlgerianMobilePhoneNumber::fromString('0699000000');
```

### API:

#### asString

To get the string value of the object:

```php
$phoneNumber->asString(); // -> '0699000000'
```

#### equals

For comparaison check:
```php
$other = AlgerianMobilePhoneNumber::fromString('0699000000');
$phoneNumber->equals($other); // -> true
```

#### isMobilis, isDjezzy and isOoreedo

To know if the object respresent a Mobilis, Djezzy or Ooreedo phone number

```php
$phoneNumber = AlgerianMobilePhoneNumber::fromString('0699000000');
$phoneNumber->isMobiles(); // -> true
$phoneNumber->isDjezzy(); // -> false
$phoneNumber->isOoreedo(); // -> false
```

#### __toString
In order to cast to object to string:
```php
$phoneNumber = AlgerianMobilePhoneNumber::fromString('0699000000');
(string)$phoneNumber; // -> '0699000000'
```

## Contribution
Any contribution are welcome to make this library better.

### Testing:
Inside the repository :

```shell
$ ./bin/phpspec run
```
