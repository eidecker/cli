# Kirby CLI

Kirby's command line interface helps you with regular tasks like the installation of the Kirby starterkit and updating your Kirby installation. It also offers a comfortable way to install templates, snippets, controllers and blueprints.

## Requirements

The Kirby CLI is being installed with Composer, the PHP package manager. For installation instructions for Composer, please visit the [Composer website](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx).

## Installation 

After installing composer, you can install Kirby CLI by running the following command:

```
composer global require "getkirby/cli=~1.0"
```

Make sure to place the ~/.composer/vendor/bin directory in your PATH so the kirby executable can be located by your system.

## Commands

### kirby install

Creates a new Kirby starterkit installation. 

```
kirby install
```

By default the starterkit will be installed in a new directory called kirby. You can specify the directory with the second argument

```
kirby install mywebsite
```

If you want to install the nightly build you can add --nightly as option

```
kirby install --nightly
```

### kirby install:core

If you've already setup your site structure and you want to add the Kirby core, you can run kirby install:core instead of kirby install

```
kirby install:core
```

The nightly option will install the core from the nightly build

```
kirby install:core --nightly
```

### kirby install:panel

If you want to add the panel to an existing installation, you can run…

```
kirby install:panel
```

The nightly option will install the panel from the nightly build

```
kirby install:panel --nightly
```

### kirby install:index.php

Sometimes it might make sense to reinstall the index.php or use this in combination with kirby install:core and kirby install:panel to create your own folder structure:

```
kirby install:index.php
```

### kirby install:htaccess

If you add the .htaccess manually or reinstall it, you can run…

```
kirby install:htaccess
```

****

### kirby update

To update an existing Kirby installation, you can run…

```
kirby update
```

This will update the kirby and panel folder, if it exists. You must run this within an existing Kirby installation, which follows Kirby's default folder structure. 

You can update your installation to the current nightly build with the --nightly option:

```
kirby update --nightly
```

****

### kirby make:blueprint

To create a boilerplate blueprint for a particular template, you can use the kirby make:blueprint command:

```
kirby make:blueprint projects
```

This will create a fresh blueprint: /site/blueprints/projects.yml

### kirby make:controller

To create a boilerplate controller for a particular template, you can use the kirby make:controller command:

```
kirby make:controller projects
```

This will create a fresh controller: /site/controllers/projects.php

### kirby make:snippet

To create a snippet, you can use the kirby make:snippet command:

```
kirby make:snippet header
```

This will create a fresh snippet: /site/snippets/header.php

### kirby make:template

To create a template, you can use the kirby make:template command:

```
kirby make:template projects
```

This will create a fresh template: /site/templates/template.php

### kirby make:user

To create a new user account, you can use the kirby make:user command:

```
kirby make:user -u home -p simpson -e homer@simpsons.com
```

The email is optional. You can also use the full option names:

```
kirby make:user --username home --password simpson --email homer@simpsons.com
```

This will create a new user in /site/accounts/homer.php

****

### kirby clear:cache

Clears the cache directory

```
kirby clear::cache
```

### kirby clear:thumbs

Delets all thumbnails in /thumbs

```
kirby clear:thumbs
```

## License 

<http://www.opensource.org/licenses/mit-license.php>

## Author

Bastian Allgeier   
<bastian@getkirby.com>  
<https://getkirby.com>  
<http://twitter.com/getkirby>