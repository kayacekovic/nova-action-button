# Nova Action Button

[![Latest Version on Packagist](https://img.shields.io/packagist/v/pdmfc/nova-action-button.svg?style=flat-square)](https://packagist.org/packages/pdmfc/nova-action-button)
![Licence](https://img.shields.io/github/license/pdmfc/nova-action-button)

This package allows you to execute an action directly on your resource table view.

## Installation

```shell
composer require pdmfc/nova-action-button
```

## Usage

```php
use App\Nova\Actions\ChangeRole;
use Pdmfc\NovaFields\ActionButton;

//...

public function fields()
{
    return [
        ActionButton::make('Action')
            ->action(ChangeRole::class, $this->id)
    ];
}
```

The `action()` method requires two params - the action class name, and the target resource id. 

![Basic example](images/basic_example.png)
---

## How to contribute

- clone the repo
- on `composer.json` of a laravel nova application add the following:

```
{
    //...

    "require" {
        "pdmfc/nova-action-button: "*"
    },

    //...
    "repositories": [
        {
            "type": "path",
            "url": "../path_to_your_package_folder"
        }
    ],
}
```

- run `composer update pdmfc/nova-action-button`

You're now ready to start contributing!