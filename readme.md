# Laravel Arabic Tafqeet  تفقيط الأرقام باللغة العربية

Laravel package to translate money numbers to our Amazing 💝 Arabic language TAFQEET . to look like [فقط تسعمائة ألف ريال و أربعة و ثلاثون هللة لاغير]
## Installation Up to Laravel 6

You can install the package via composer:

	composer require alkoumi/laravel-arabic-tafqeet

The service provider will automatically get registered. Or you may manually add the service provider in your `config/app.php` file:

    'providers' => [
        // ...
        Alkoumi\CarbonDateTranslator\LaravelArabicTafqeetServiceProvider::class,
    ];

## Usage

Simply pass an instance of carbon date to the method Tafqeet::inArabic()

```php

	$money = App\cheque::first()->money;
	$differenceInArabic = Tafqeet::inArabic($money);

        // Result => "فقط تسعمائة ألف ريال و أربعة و ثلاثون هللة لاغير"
```