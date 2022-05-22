## Whats Under the hood

```php
php artisan adminlte:status
Checking the resources installation ...
 7/7 [============================] 100%
All resources checked succesfully!

+------------------+------------------------------------------+-----------+----------+
| Package Resource | Description                              | Status    | Required |
+------------------+------------------------------------------+-----------+----------+
| assets           | The AdminLTE required assets             | Installed | true     |
| config           | The default package configuration file   | Installed | true     |
| translations     | The default package translations files   | Installed | true     |
| main_views       | The default package main views           | Installed | false    |
| auth_views       | The default package authentication views | Installed | false    |
| basic_views      | The default package basic views          | Installed | false    |
| basic_routes     | The package routes                       | Installed | false    |
+------------------+------------------------------------------+-----------+----------+

Status legends:
+---------------+----------------------------------------------------------------------------------------------+
| Status        | Description                                                                                  |
+---------------+----------------------------------------------------------------------------------------------+
| Installed     | The resource is installed and matches with the default package resource                      |
| Mismatch      | The installed resource mismatch the package resource (update available or resource modified) |
| Not Installed | The package resource is not installed                                                        |
+---------------+----------------------------------------------------------------------------------------------+
```
