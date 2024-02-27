# Aplikasi Point Of Sale Ci4
[![N|Solid]([https://cldup.com/dTxpPi9lDf.thumb.png](https://www.google.com/search?q=monkey+d+luffy+egghead&tbm=isch&ved=2ahUKEwiohdKo8MuEAxXPk2MGHQA1DMQQ2-cCegQIABAA&oq=monkey+d+luffy+egghead&gs_lp=EgNpbWciFm1vbmtleSBkIGx1ZmZ5IGVnZ2hlYWQyBxAAGIAEGBhInS5QlwVYxSxwAngAkAEAmAHlAaABjQiqAQU5LjEuMbgBA8gBAPgBAYoCC2d3cy13aXotaW1nwgIEECMYJ8ICCBAAGIAEGLEDwgIFEAAYgATCAhAQABiABBiKBRhDGLEDGIMBwgIKEAAYgAQYigUYQ8ICBBAAGB6IBgE&sclient=img&ei=WAXeZaj5Kc-njuMPgOqwoAw&bih=651&biw=1366&rlz=1C1ONGR_enID1012ID1012#imgrc=8CY9Xi4mqxtJRM))](https://nodesource.com/products/nsolid)

## What is CodeIgniter?

CodeIgniter is a PHP full-stack web framework that is light, fast, flexible and secure.
More information can be found at the [official site](https://codeigniter.com).

This repository holds a composer-installable app starter.
It has been built from the
[development repository](https://github.com/codeigniter4/CodeIgniter4).

More information about the plans for version 4 can be found in [CodeIgniter 4](https://forum.codeigniter.com/forumdisplay.php?fid=28) on the forums.

The user guide corresponding to the latest version of the framework can be found
[here](https://codeigniter4.github.io/userguide/).

## Installation & updates

`composer create-project codeigniter4/appstarter` then `composer update` whenever
there is a new release of the framework.

When updating, check the release notes to see if there are any changes you might need to apply
to your `app` folder. The affected files can be copied or merged from
`vendor/codeigniter4/framework/app`.

## Setup

Copy `env` to `.env` and tailor for your app, specifically the baseURL
and any database settings.

## Important Change with index.php

`index.php` is no longer in the root of the project! It has been moved inside the *public* folder,
for better security and separation of components.

This means that you should configure your web server to "point" to your project's *public* folder, and
not to the project root. A better practice would be to configure a virtual host to point there. A poor practice would be to point your web server to the project root and expect to enter *public/...*, as the rest of your logic and the
framework are exposed.

**Please** read the user guide for a better explanation of how CI4 works!

## Repository Management

We use GitHub issues, in our main repository, to track **BUGS** and to track approved **DEVELOPMENT** work packages.
We use our [forum](http://forum.codeigniter.com) to provide SUPPORT and to discuss
FEATURE REQUESTS.

This repository is a "distribution" one, built by our release preparation script.
Problems with it can be raised on our forum, or as issues in the main repository.

## Server Requirements

PHP version 7.4 or higher is required, with the following extensions installed:

- [intl](http://php.net/manual/en/intl.requirements.php)
- [mbstring](http://php.net/manual/en/mbstring.installation.php)

> **Warning**
> The end of life date for PHP 7.4 was November 28, 2022. If you are
> still using PHP 7.4, you should upgrade immediately. The end of life date
> for PHP 8.0 will be November 26, 2023.

Additionally, make sure that the following extensions are enabled in your PHP:

- json (enabled by default - don't turn it off)
- [mysqlnd](http://php.net/manual/en/mysqlnd.install.php) if you plan to use MySQL
- [libcurl](http://php.net/manual/en/curl.requirements.php) if you plan to use the HTTP\CURLRequest library
