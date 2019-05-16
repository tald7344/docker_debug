# Using PHP CodeSniffer With WordPress

### Prerequisites :
* a version of PHP (preferably 5.6.10 or later)
* PHP CodeSniffer
* Composer

### Install the WordPress Rules
1. Remember to create composer.json in the root of your project and include a dependency for `squizlabs/php_codesniffer`:
```json
{
    "require": {
        "squizlabs/php_codesniffer": "2.*"
    }
}
```

2. Once done Run The command `$ composer update` , To verify the installation, run the command `$ vendor/bin/phpcs --version`:

3. For installing the WordPress rules, Run the following command within the root directory of your project :
```composer
composer create-project wp-coding-standards/wpcs:dev-master --no-dev
```

Note that you may be prompted with the following question:

    Do you want to remove the existing VCS (.git, .svn..) history? [Y,n]?

If you know what you're doing, then feel free to go ahead and select 'n'; otherwise, you'll be fine hitting 'y'.

### Add the Rules to PHP CodeSniffer :
1. Now that PHP CodeSniffer is installed, and the WordPress rules are installed, we need to make sure PHP CodeSniffer is aware of our new ruleset. 
From the root of your project directory, enter the following command :
```
$ vendor/bin/phpcs --config-set installed_paths wpcs
```
2. To verify that the new rules have been added enter the following command:
```
$ vendor/bin/phpcs -i
```

### Running PHP CodeSniffer Against WordPress Projects
1. To run PHP CodeSniffer with the WordPress rules against the files in the plugin directory, enter the following command in the Terminal:
```
$ vendor/bin/phpcs --standard=WordPress fileName
```