# yii2-authclient-microsoft

Yii2 authclient for Microsoft 365/Azure

## Installation

With Composer :


```sh
composer require pde159/yii2-authclient-microsoft
```

or add to "require" section to composer.json

```sh
"pde159/yii2-authclient-microsoft": "*"
```

## Usage

First create you Application via Microsoft Azure Portal and configure :

- a redirect URI
- a secret key
- set to `all tenant` for multitenant availability

And add the Oauth2 client to your Yii2 configuration `component` section

```php
'components' => [
    'authClientCollection' => [
        'class'   => \yii\authclient\Collection::className(),
        'clients' => [
            'microsoft' => [
                'class'         => 'pde159\authclient\Microsoft',
                'returnUrl'     => 'http://localhost/user/login',
                'clientId'      => 'clientIDyoudefinedInAzurePortal',
                'clientSecret'  => 'SecretyoucratedinAzurePortal',
            ],
            ...
        ],
    ],
    ...
]
```
## Donations:
* Donation is as per your goodwill to support my development.
* If you are interested in my future developments, i would really appreciate a small donation to support this project.
* 
```html
My revolut acount
https://revolut.me/marcin1k25
```
[![Send mone to my revolut acount](https://revolut.me/marcin1k25)](https://revolut.me/marcin1k25)
