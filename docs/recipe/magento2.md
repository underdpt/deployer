<!-- DO NOT EDIT THIS FILE! -->
<!-- Instead edit recipe/magento2.php -->
<!-- Then run bin/docgen -->

# magento2

[Source](/recipe/magento2.php)

* Requires
  * [common](/docs/recipe/common.md)

## Configuration
### static_content_locales
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L20)

By default setup:static-content:deploy uses `en_US`.
To change that, simply put `set('static_content_locales', 'en_US de_DE');`
in you deployer script.

```php title="Default value"
'en_US'
```


### content_version
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L22)





### shared_files
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L26)

Overrides [shared_files](/docs/recipe/deploy/shared.md#shared_files) from `recipe/deploy/shared.php`.



```php title="Default value"
[
    'app/etc/env.php',
    'var/.maintenance.ip',
    'var/.maintenance.flag'
]
```


### shared_dirs
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L31)

Overrides [shared_dirs](/docs/recipe/deploy/shared.md#shared_dirs) from `recipe/deploy/shared.php`.



```php title="Default value"
[
    'var/composer_home',
    'var/log',
    'var/export',
    'var/report',
    'var/import',
    'var/import_history',
    'var/session',
    'var/importexport',
    'var/backups',
    'var/tmp',
    'pub/sitemap',
    'pub/media'
]
```


### writable_dirs
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L45)

Overrides [writable_dirs](/docs/recipe/deploy/writable.md#writable_dirs) from `recipe/deploy/writable.php`.



```php title="Default value"
[
    'var',
    'pub/static',
    'pub/media',
    'generated'
]
```


### clear_paths
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L51)

Overrides [clear_paths](/docs/recipe/deploy/clear_paths.md#clear_paths) from `recipe/deploy/clear_paths.php`.



```php title="Default value"
[
    'generated/*',
    'pub/static/_cache/*',
    'var/generation/*',
    'var/cache/*',
    'var/page_cache/*',
    'var/view_preprocessed/*'
]
```


### magento_version
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L60)





### maintenance_mode_status_active
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L67)






## Tasks

### magento:compile
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L75)

Compiles magento di.

Tasks


### magento:deploy:assets
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L82)

Deploys assets.




### magento:sync:content_version
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L87)

Syncs content version.




### magento:maintenance:enable
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L97)

Enables maintenance mode.




### magento:maintenance:disable
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L102)

Disables maintenance mode.




### magento:config:import
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L107)

Config Import.




### magento:upgrade:db
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L142)

Upgrades magento database.




### magento:cache:flush
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L169)

Flushes Magento Cache.




### deploy:magento
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L174)

Magento2 deployment operations.




This task is group task which contains next tasks:
* [magento:build](/docs/recipe/magento2.md#magentobuild)
* [magento:config:import](/docs/recipe/magento2.md#magentoconfigimport)
* [magento:upgrade:db](/docs/recipe/magento2.md#magentoupgradedb)
* [magento:cache:flush](/docs/recipe/magento2.md#magentocacheflush)


### magento:build
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L182)

Magento2 build operations.




This task is group task which contains next tasks:
* [magento:compile](/docs/recipe/magento2.md#magentocompile)
* [magento:deploy:assets](/docs/recipe/magento2.md#magentodeployassets)


### deploy
[Source](https://github.com/deployphp/deployer/blob/master/recipe/magento2.php#L188)

Deploys your project.




This task is group task which contains next tasks:
* [deploy:prepare](/docs/recipe/common.md#deployprepare)
* [deploy:vendors](/docs/recipe/deploy/vendors.md#deployvendors)
* [deploy:clear_paths](/docs/recipe/deploy/clear_paths.md#deployclear_paths)
* [deploy:magento](/docs/recipe/magento2.md#deploymagento)
* [deploy:publish](/docs/recipe/common.md#deploypublish)


