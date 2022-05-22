https://laravel.com/docs/9.x
`laravel new PROJECT_NAME`

https://github.com/laravel/ui
`composer require laravel/ui`

`php artisan ui bootstrap --auth`

https://github.com/barryvdh/laravel-debugbar
`composer require barryvdh/laravel-debugbar --dev`

## Follow Here:

https://github.com/jeroennoten/Laravel-AdminLTE/wiki/Installation

`composer require jeroennoten/laravel-adminlte`

`php artisan adminlte:install --force`

`php artisan adminlte:status`

```php
Checking the resources installation ...
 7/7 [============================] 100%
All resources checked succesfully!

+------------------+------------------------------------------+---------------+----------+
| Package Resource | Description                              | Status        | Required |
+------------------+------------------------------------------+---------------+----------+
| assets           | The AdminLTE required assets             | Installed     | true     |
| config           | The default package configuration file   | Installed     | true     |
| translations     | The default package translations files   | Installed     | true     |
| main_views       | The default package main views           | Not Installed | false    |
| auth_views       | The default package authentication views | Mismatch      | false    |
| basic_views      | The default package basic views          | Mismatch      | false    |
| basic_routes     | The package routes                       | Not Installed | false    |
+------------------+------------------------------------------+---------------+----------+

Status legends:
+---------------+----------------------------------------------------------------------------------------------+
| Status        | Description                                                                                  |
+---------------+----------------------------------------------------------------------------------------------+
| Installed     | The resource is installed and matches with the default package resource                      |
| Mismatch      | The installed resource mismatch the package resource (update available or resource modified) |
| Not Installed | The package resource is not installed                                                        |
+---------------+----------------------------------------------------------------------------------------------+
```
In the particular case the update includes jumping to a new version of the underlying AdminLTE package, you may also want to update the plugins you have previously installed using the command `php artisan adminlte:plugins install --plugin=somePlugin`. In these cases, you may proceed as explained below.

Execute the command `php artisan adminlte:plugins` to get a status overview of the previously installed plugins.

For those ones you see the mismatch legend on the status column, you may want to update the plugin executing the next command:

`php artisan adminlte:plugins install --plugin=thePluginKeyWithMismatchLegend`



`php artisan adminlte:install --only=auth_views`

```php
php artisan adminlte:status
Checking the resources installation ...
 7/7 [============================] 100%
All resources checked succesfully!

+------------------+------------------------------------------+---------------+----------+
| Package Resource | Description                              | Status        | Required |
+------------------+------------------------------------------+---------------+----------+
| assets           | The AdminLTE required assets             | Installed     | true     |
| config           | The default package configuration file   | Installed     | true     |
| translations     | The default package translations files   | Installed     | true     |
| main_views       | The default package main views           | Not Installed | false    |
| auth_views       | The default package authentication views | Installed     | false    |
| basic_views      | The default package basic views          | Mismatch      | false    |
| basic_routes     | The package routes                       | Not Installed | false    |
+------------------+------------------------------------------+---------------+----------+

Status legends:
+---------------+----------------------------------------------------------------------------------------------+      
| Status        | Description                                                                                  |      
+---------------+----------------------------------------------------------------------------------------------+      
| Installed     | The resource is installed and matches with the default package resource                      |      
| Mismatch      | The installed resource mismatch the package resource (update available or resource modified) |      
| Not Installed | The package resource is not installed                                                        |      
+---------------+----------------------------------------------------------------------------------------------+ 
```

`php artisan adminlte:plugins install --plugin=icheckBootstrap`

```php
php artisan adminlte:plugins install --plugin=icheckBootstrap
 1/1 [============================] 100%
The plugins installation is complete. Summary:

+-----------------+-----------+
| Plugin Key      | Status    |
+-----------------+-----------+
| icheckBootstrap | Installed |
+-----------------+-----------+
```
`https://github.com/jeroennoten/Laravel-AdminLTE/issues/1102` my request

* Read (reply)
`https://github.com/jeroennoten/Laravel-AdminLTE/wiki/Artisan-Console-Commands` 

to check how you may install additional resources. However, note you may not want to publish all the package resources (read carefully what each one provides). Usually, the required resources are enough to start, then you may publish the auth_views if you want to implement an authentication scaffolding, and the main_views if you want to make any customization on the blade views provided by the package.

