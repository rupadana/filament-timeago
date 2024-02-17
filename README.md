# This is my package filament-timeago

[![Latest Version on Packagist](https://img.shields.io/packagist/v/rupadana/filament-timeago.svg?style=flat-square)](https://packagist.org/packages/rupadana/filament-timeago)
[![GitHub Tests Action Status](https://img.shields.io/github/actions/workflow/status/rupadana/filament-timeago/run-tests.yml?branch=main&label=tests&style=flat-square)](https://github.com/rupadana/filament-timeago/actions?query=workflow%3Arun-tests+branch%3Amain)
[![GitHub Code Style Action Status](https://img.shields.io/github/actions/workflow/status/rupadana/filament-timeago/fix-php-code-style-issues.yml?branch=main&label=code%20style&style=flat-square)](https://github.com/rupadana/filament-timeago/actions?query=workflow%3A"Fix+PHP+code+style+issues"+branch%3Amain)
[![Total Downloads](https://img.shields.io/packagist/dt/rupadana/filament-timeago.svg?style=flat-square)](https://packagist.org/packages/rupadana/filament-timeago)



Display the age of each record, indicating when it was created, updated, and (if applicable) deleted.

## Installation

You can install the package via composer:

```bash
composer require rupadana/filament-timeago
```


## Usage

```php
public static function table(Table $table): Table
{
    return $table
        ->columns([
            TimeAgoColumn::make('created_at')
                ->dateLabel(
                    years: 'years',
                    months: 'months',
                    days: 'days',
                    hours: 'hours',
                    minutes: 'minutes',
                    seconds: 'seconds'
                ) // Optional
                ->interval(1000) // Optional, default : 0
                ->prefixText('string') // Optional
                ->suffixText('string') // Optional
        ])
}
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Security Vulnerabilities

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits

- [Rupadana](https://github.com/rupadana)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
