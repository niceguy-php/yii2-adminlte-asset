AdminLTE Asset Bundle
=====================

*Backend UI for Yii2 Framework, based on [AdminLTE](https://github.com/almasaeed2010/AdminLTE)*

!["Yii2 AdminLTE Presentation"](https://cloud.githubusercontent.com/assets/874234/7603896/753228ee-f943-11e4-9d42-2a31b41eb42d.jpg)

This package contains an [Asset Bundle for Yii 2.0 Framework](http://www.yiiframework.com/doc-2.0/guide-structure-assets.html) 
which registers the CSS files for the AdminLTE user-interface.

The CSS files are installed via Yii's recommended usage of the `fxp/composer-asset-plugin`.


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

To install AdminLTE v2 run:

```
php composer.phar require dmstr/yii2-adminlte-asset "2.*"
```

To install AdminLTE v1 run:

```
php composer.phar require dmstr/yii2-adminlte-asset "1.*"
```



Quick Start
-----------

Once the extension is installed, you can have a *preview* by reconfiguring the path mappings of the view component:

For Yii 2 [Application Template](https://github.com/yiisoft/yii2-app-advanced) or [Basic Application Template](https://github.com/yiisoft/yii2-app-basic)

```php
'components' => [
    'view' => [
         'theme' => [
             'pathMap' => [
                '@app/views' => '@vendor/dmstr/yii2-adminlte-asset/example-views/yiisoft/yii2-app'
             ],
         ],
    ],
],
```


For [Phundament 4](https://github.com/phundament/app)

```php
'components' => [
    'view' => [
        'theme' => [
            'pathMap' => [
                '@app/views' => '@vendor/dmstr/yii2-adminlte-asset/example-views/phundament/app'
            ],
        ],
    ],
],
```

This asset bundle provides sample files for layout and view (see folder `examples/`), they are **not meant to be customized directly in the `vendor/` folder**.

Therefore it is recommended to **copy the views into your application** and adjust them to your needs.


Customization
-------------

- Copy files from `vendor/dmstr/yii2-adminlte-asset/example-views/yiisoft/yii2-app` (or other theme) to `@app/views`.
- Remove the custom `view` configuration from your application by deleting the path mappings, if you have made them before.
- Edit your views adhering to html markup `vendor/almasaeed2010/adminlte/pages`

By default the extension uses blue skin for AdminLTE. You can change this. Just replace class of body `skin-blue`. Here is the list of available skins:

```
"skin-blue",
"skin-black",
"skin-red",
"skin-yellow",
"skin-purple",
"skin-green",
"skin-blue-light",
"skin-black-light",
"skin-red-light",
"skin-yellow-light",
"skin-purple-light",
"skin-green-light"
```

For more information, please read https://almsaeedstudio.com/themes/AdminLTE/documentation/index.html

> Namespacing rules follow the Yii 2.0 framework structure, eg. `dmstr\web` for the Asset Bundle.
 
