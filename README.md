# moodle_hello_world
Moodle 3.11 Plugin Hello World.
This simple plugin prints "Hello World!" inside Moodle.


## Moodle Local Plugin Installation Guide
- Start your php server and database (for example, you can use XAMPP
  https://www.apachefriends.org/it/index.html)
- Download last Moodle version (Moodle 3.11 requires php 7.4)
- Unzip it
- Put it into htdocs folder
- Follow Moodle installation guide (the DB used in xampp is MariaDB with
  "root" as username and void password by default)
- Place your plugin folder under local folder (inside Moodle folder)
  - Notice: Plugin folder name cannot contain '-' or any space ('_' only is allowed)
- Name the namespace accordingly inside your code (namespace must be the same
  of the plugin folder)
- Build the plugin: ```php admin/cli/upgrade.php```
- Reload Moodle in Browser
- Purge the plugin after code change: ```php admin/cli/purge_caches.php```


## Moodle Local Plugin Uninstallation Guide
This operation is needed when a change in DB structure occurs, in order to
reinstall the Plugin with the current DB schema.
- Uninstall the Plugin via php: ```php admin/cli/uninstall_plugins.php
  --plugins=<plugin_name> --run```


## Dependencies

1. Moodle: https://moodle.org/

## Contacts

Agnese Salutari – agneses92@hotmail.it

Distributed under the GNU General Public License v3.0. See ``LICENSE`` for more information.

[https://github.com/agnsal](https://github.com/agnsal)


## Contributing

1. Fork it (<https://github.com/yourname/yourproject/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request