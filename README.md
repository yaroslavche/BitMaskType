[![Build Status](https://travis-ci.org/yaroslavche/BitMaskType.svg?branch=master)](https://travis-ci.org/yaroslavche/BitMaskType)
[![codecov](https://codecov.io/gh/yaroslavche/bitmasktype/branch/master/graph/badge.svg)](https://codecov.io/gh/yaroslavche/bitmasktype)

# BitMaskType

[BitMask](https://github.com/yaroslavche/BitMask) Doctrine Type

## Getting Started

For using Doctrine mapping type as `bitmask` need to register type. See example [in Doctrine documentation](https://www.doctrine-project.org/projects/doctrine-orm/en/latest/cookbook/custom-mapping-types.html)

For Symfony need only add custom type in Doctrine config:
```yaml
# config/packages/doctrine.yaml

doctrine:
    dbal:
        types:
            bitmask: BitMask\Doctrine\Types\BitMaskType
```

[Usage example](https://medium.com/@yaroslav429/symfony-4-doctrine-custom-mapping-type-1c8ff679f4c1)

### Installing

Install package via [composer](https://getcomposer.org/) 
```bash
composer require yaroslavche/bitmasktype
```

## Scripts:
#### Tests
PHPUnit
```bash
$ composer phpunit
$ ./vendor/bin/phpunit
```
Infection (src without mutable code, so infection is disabled)
```bash
$ composer infection
$ ./vendor/bin/infection --min-msi=50 --min-covered-msi=70
```
#### PHPStan
```bash
$ composer phpstan
$ ./vendor/bin/phpstan analyse src/ -c phpstan.neon --level=7 --no-progress -vvv --memory-limit=1024M
```
#### PHP-CS
```bash
$ composer cscheck
$ ./vendor/bin/phpcs
```
```bash
$ composer csfix
$ ./vendor/bin/phpcbf
```

## Contributing

Feel free to fork or contribute =)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
